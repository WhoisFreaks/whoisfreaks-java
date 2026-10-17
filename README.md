# WhoisFreaks Java SDK: WHOIS API Client for Java

[![Maven Central](https://img.shields.io/maven-central/v/com.whoisfreaks/whoisfreaks.svg)](https://central.sonatype.com/artifact/com.whoisfreaks/whoisfreaks)
[![License: MIT](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![API status](https://img.shields.io/badge/API%20status-live-brightgreen.svg)](https://status.whois.whoisfreaks.com/)

The official Java client for the [WhoisFreaks WHOIS API](https://whoisfreaks.com/products/whois-api). Look up live WHOIS records for any domain across 1,529+ TLDs, pull WHOIS history back to 1986, search registrants with reverse WHOIS and run bulk WHOIS lookups from Java code.

The same package covers the [DNS lookup API](https://whoisfreaks.com/products/dns-checker-api), [domain availability API](https://whoisfreaks.com/products/domain-availability-api), [typosquatting API](https://whoisfreaks.com/products/domain-typosquats-api), [SSL certificate API](https://whoisfreaks.com/products/ssl-certificate-api), IP geolocation and IP reputation.

A live WHOIS lookup returns structured JSON like this (trimmed):

```json
{
  "status": true,
  "domain_name": "whoisfreaks.com",
  "domain_registered": "yes",
  "create_date": "2019-03-19",
  "update_date": "2026-02-17",
  "expiry_date": "2027-03-19",
  "domain_registrar": {
    "iana_id": "1068",
    "registrar_name": "NAMECHEAP INC",
    "normalized_name": "namecheap, inc.",
    "website_url": "http://www.namecheap.com"
  },
  "registrant_contact": {
    "city": "Lewes",
    "state": "Delaware",
    "zip_code": "19958",
    "country_name": "United States",
    "country_code": "US"
  },
  "name_servers": ["albert.ns.cloudflare.com", "sue.ns.cloudflare.com"],
  "domain_status": ["clienttransferprohibited"]
}
```

## Contents

- [Installation](#installation)
- [Get an API key](#get-an-api-key)
- [WHOIS lookup](#whois-lookup)
- [Normalized registrar, address and date fields](#normalized-registrar-address-and-date-fields)
- [Bulk WHOIS lookup](#bulk-whois-lookup)
- [WHOIS history](#whois-history)
- [Reverse WHOIS](#reverse-whois)
- [DNS lookup](#dns-lookup)
- [Domain availability check](#domain-availability-check)
- [Typosquatting detection](#typosquatting-detection)
- [Error handling](#error-handling)
- [All endpoints](#all-endpoints)
- [Requirements](#requirements)
- [Support](#support)

## Installation

Maven:

```xml
<dependency>
  <groupId>com.whoisfreaks</groupId>
  <artifactId>whoisfreaks</artifactId>
  <version>0.24.0</version>
</dependency>
```

Gradle:

```groovy
implementation "com.whoisfreaks:whoisfreaks:0.24.0"
```

## Get an API key

Create a free account at [billing.whoisfreaks.com/signup](https://billing.whoisfreaks.com/signup). New accounts get 500 free credits with no credit card, usable across the live WHOIS, WHOIS history and reverse WHOIS APIs.

Keep the key out of source control. The examples read it from an environment variable:

```sh
export WHOISFREAKS_API_KEY="your_api_key"
```

Every example below assumes this setup:

```java
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.ApiKeyAuth;
import com.whoisfreaks.client.api.*;
import com.whoisfreaks.client.model.*;
import java.util.Arrays;

ApiClient client = Configuration.getDefaultApiClient();
ApiKeyAuth auth = (ApiKeyAuth) client.getAuthentication("ApiKeyAuth");
auth.setApiKey(System.getenv("WHOISFREAKS_API_KEY"));
```

## WHOIS lookup

Each request queries WHOIS servers and RDAP live, so you get the current record rather than a cached copy. One lookup costs 1 credit.

```java
WhoisApi whois = new WhoisApi(client);
WhoisResponse record = whois.whoisLive("whoisfreaks.com", "json");

System.out.println(record.getCreateDate() + " " + record.getExpiryDate()); // 2019-03-19 2027-03-19
System.out.println(record.getDomainRegistrar().getRegistrarName());        // NAMECHEAP INC
System.out.println(record.getNameServers());
```

## Normalized registrar, address and date fields

Registries and registrars write the same facts in different formats. The API returns normalized fields so records from different TLDs line up without your own parsing code.

| What you get | Field | Example |
|---|---|---|
| One registrar name, however the registry spells it | `domain_registrar.normalized_name` | `namecheap, inc.` for both "NAMECHEAP INC" and "NameCheap, Inc" |
| A parsed and geocoded contact address | `registrant_contact.street`, `city`, `state`, `zip_code`, `country_name`, `country_code` | `Lewes`, `Delaware`, `19958`, `United States`, `US` |
| One date format | `create_date`, `update_date`, `expiry_date` | `2019-03-19` |

```java
PersonalInformation registrant = record.getRegistrantContact();

System.out.println(record.getDomainRegistrar().getNormalizedName()); // namecheap, inc.
System.out.println(registrant.getCity() + " " + registrant.getState()); // Lewes Delaware
System.out.println(registrant.getCountryCode());                     // US
```

Use these fields to group a domain portfolio by registrar, filter registrants by country code or sort domains by expiry date across every TLD.

## Bulk WHOIS lookup

Look up to 100 domains in one call.

```java
BulkWhoisRequest request = new BulkWhoisRequest()
    .domainNames(Arrays.asList("example.com", "whoisfreaks.com", "github.com"));
BulkWhoisResponse result = whois.bulkWhois(request, "json");
```

For larger jobs, the [Bulk WHOIS API](https://whoisfreaks.com/products/bulk-whois-api) accepts file uploads of up to 3M domains.

## WHOIS history

Get every recorded ownership change for a domain in one request. A new record is stored only when the WHOIS data changed, and history goes back to 1986.

```java
WhoisHistoricalResponse history = whois.whoisHistory("whoisfreaks.com", "json");
```

## Reverse WHOIS

Find every domain registered with a keyword, such as a company name or registrant email, across 4.5B+ WHOIS records.

```java
ReverseWhoisResponse matches = whois.whoisReverse("whoisfreaks", 1, "json");
```

## DNS lookup

Pull live DNS records for a domain. Pass `all` or a comma-separated list of record types: `A`, `AAAA`, `MX`, `NS`, `TXT`, `SOA`, `SPF`, `CNAME`.

```java
DnsResponse records = new DnsApi(client).dnsLive("A,MX,TXT", "whoisfreaks.com", null, "json");
```

The same class also covers bulk DNS, historical DNS and reverse DNS lookups.

## Domain availability check

Check whether a domain is registered and, with suggestions turned on, get up to 100 available alternatives on other TLDs.

```java
DomainAvailabilityResponse result =
    new DomainAvailabilityApi(client).domainAvailabilityV2("whoisfreaks.io", true, 5, "json");
```

## Typosquatting detection

Find registered domains that look like typo variants of a brand name. Search by a brand `keyword`, or by a wildcard `pattern` such as `whois*` (up to 3 asterisks). Results come 100 domains per page with registration date, expiry date and drop status, across 1,529+ TLDs.

```java
TyposquattingResponse typos = new TyposquattingApi(client).typosquatting("whoisfreaks", null, null);
```

To get the next page, pass the `nextPageToken` value from the response as `pageToken`, along with the same keyword or pattern.

## Error handling

Failed requests raise `ApiException` with the HTTP status code and response body.

```java
try {
  WhoisResponse record = whois.whoisLive("whoisfreaks.com", "json");
} catch (ApiException e) {
  System.err.println(e.getCode() + " " + e.getResponseBody());
}
```

Live API uptime and incident history are on the [status page](https://status.whois.whoisfreaks.com/).

## All endpoints

All URIs are relative to `https://api.whoisfreaks.com`. Each method links to its parameters and response model.

### WHOIS

| Class | Method | HTTP request | Description |
|---|---|---|---|
| WhoisApi | [bulkWhois](docs/WhoisApi.md#bulkwhois) | POST /v2.0/bulkwhois/live | Bulk WHOIS Lookup |
| WhoisApi | [whoisHistory](docs/WhoisApi.md#whoishistory) | GET /v2.0/whois/history | Historical WHOIS records for a domain |
| WhoisApi | [whoisLive](docs/WhoisApi.md#whoislive) | GET /v2.0/whois/live | Live WHOIS Lookup |
| WhoisApi | [whoisReverse](docs/WhoisApi.md#whoisreverse) | GET /v2.0/whois/reverse | Reverse WHOIS lookup by keyword |
| AsnWhoisApi | [asnWhois](docs/AsnWhoisApi.md#asnwhois) | GET /v2.0/asn-whois | ASN WHOIS Lookup |
| IpWhoisApi | [ipWhois](docs/IpWhoisApi.md#ipwhois) | GET /v1.0/ip-whois | IP WHOIS Lookup |

### DNS, SSL and subdomains

| Class | Method | HTTP request | Description |
|---|---|---|---|
| DnsApi | [dnsBulk](docs/DnsApi.md#dnsbulk) | POST /v2.0/dns/bulk/live | Bulk DNS Lookup |
| DnsApi | [dnsHistorical](docs/DnsApi.md#dnshistorical) | GET /v2.0/dns/historical | Historical DNS Lookup |
| DnsApi | [dnsLive](docs/DnsApi.md#dnslive) | GET /v2.0/dns/live | Live DNS Lookup |
| DnsApi | [dnsReverse](docs/DnsApi.md#dnsreverse) | GET /v2.1/dns/reverse | Reverse DNS Lookup |
| SslApi | [sslLookup](docs/SslApi.md#ssllookup) | GET /v1.0/ssl/live | SSL Certificate Lookup |
| SubdomainsApi | [subdomains](docs/SubdomainsApi.md#subdomains) | GET /v1.0/subdomains | Subdomains Lookup |

### Domain availability, typosquatting and reputation

| Class | Method | HTTP request | Description |
|---|---|---|---|
| DomainAvailabilityApi | [bulkDomainAvailabilityV2](docs/DomainAvailabilityApi.md#bulkdomainavailabilityv2) | POST /v2.0/domain/availability | Bulk Domain Availability Check |
| DomainAvailabilityApi | [domainAvailabilityV2](docs/DomainAvailabilityApi.md#domainavailabilityv2) | GET /v2.0/domain/availability | Domain Availability Check with Suggestions |
| TyposquattingApi | [typosquatting](docs/TyposquattingApi.md#typosquatting) | GET /v3.0/domain/typos | Typosquatting Lookup |
| DomainReputationApi | [domainReputation](docs/DomainReputationApi.md#domainreputation) | GET /v1/domain/security | Domain Reputation Lookup |

### IP geolocation and reputation

| Class | Method | HTTP request | Description |
|---|---|---|---|
| GeolocationApi | [bulkGeolocation](docs/GeolocationApi.md#bulkgeolocation) | POST /v1.0/geolocation | Bulk IP Geolocation |
| GeolocationApi | [geolocation](docs/GeolocationApi.md#geolocation) | GET /v1.0/geolocation | IP Geolocation Lookup |
| IpReputationApi | [bulkIpReputation](docs/IpReputationApi.md#bulkipreputation) | POST /v1.0/security | Bulk IP Reputation |
| IpReputationApi | [ipReputation](docs/IpReputationApi.md#ipreputation) | GET /v1.0/security | IP Reputation Lookup |

### Account

| Class | Method | HTTP request | Description |
|---|---|---|---|
| AccountApi | [accountUsage](docs/AccountApi.md#accountusage) | GET /v1.0/whoisapi/usage | Account Usage |
| AccountApi | [databaseFileStatus](docs/AccountApi.md#databasefilestatus) | GET /v3.4/status | Database File Status (Public) |
| AccountApi | [rotateApiKey](docs/AccountApi.md#rotateapikey) | GET /v1.0/api-key/rotate | Rotate API Key |

### Database downloads

WHOIS, DNS, subdomain, IP, newly registered, expiring and dropped domain databases, plus the phishing, malware and spam threat feeds, are available through the `Databases*` classes. See the [full method list](docs/) for every download and status endpoint.

## Requirements

Java 8 or later. Maven 3.8.3+ or Gradle 7.2+.

## Support

- WHOIS API documentation: [whoisfreaks.com/documentation/whois-api](https://whoisfreaks.com/documentation/whois-api)
- All API documentation: [whoisfreaks.com/documentation](https://whoisfreaks.com/documentation)
- Product page: [WhoisFreaks WHOIS API](https://whoisfreaks.com/products/whois-api)
- API status: [status.whois.whoisfreaks.com](https://status.whois.whoisfreaks.com/)
- Email: support@whoisfreaks.com
- Quick start: [WHOIS API examples](https://github.com/WhoisFreaks/whois-api)
- Other languages: [Python](https://github.com/WhoisFreaks/whoisfreaks-python), [JavaScript](https://github.com/WhoisFreaks/whoisfreaks-javascript), [TypeScript](https://github.com/WhoisFreaks/whoisfreaks-typescript), [Java](https://github.com/WhoisFreaks/whoisfreaks-java), [Go](https://github.com/WhoisFreaks/whoisfreaks-go), [C#](https://github.com/WhoisFreaks/whoisfreaks-csharp), [Ruby](https://github.com/WhoisFreaks/whoisfreaks-ruby), [PHP](https://github.com/WhoisFreaks/whoisfreaks-php), [Swift](https://github.com/WhoisFreaks/whoisfreaks-swift), [Kotlin](https://github.com/WhoisFreaks/whoisfreaks-kotlin)

## License

MIT. See [LICENSE](LICENSE).
