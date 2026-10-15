

# DnsRecord

Union of all DNS record variants (A/AAAA/MX/NS/CNAME/PTR/TXT/SPF/SOA).

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**type** | **Integer** | Numeric DNS record type: 1 A, 2 NS, 5 CNAME, 6 SOA, 12 PTR, 15 MX, 16 TXT, 28 AAAA, 99 SPF. |  [optional] |
|**dnsType** | **String** | Record type name, e.g. A, MX, TXT |  [optional] |
|**name** | **String** |  |  [optional] |
|**ttl** | **Integer** |  |  [optional] |
|**rawText** | **String** | The record in zone-file format |  [optional] |
|**rRsetType** | **Integer** |  |  [optional] |
|**singleName** | **String** | Target host for NS, CNAME and PTR records |  [optional] |
|**address** | **String** |  |  [optional] |
|**priority** | **Integer** |  |  [optional] |
|**exchange** | **String** |  |  [optional] |
|**target** | **String** |  |  [optional] |
|**strings** | **List&lt;String&gt;** |  |  [optional] |
|**host** | **String** |  |  [optional] |
|**admin** | **String** |  |  [optional] |
|**serial** | **Long** | SOA serial; values above 2^31 are common, so it is 64-bit |  [optional] |
|**refresh** | **Integer** |  |  [optional] |
|**retry** | **Integer** |  |  [optional] |
|**expire** | **Integer** |  |  [optional] |
|**minimum** | **Integer** |  |  [optional] |



