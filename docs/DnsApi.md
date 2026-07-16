# DnsApi

All URIs are relative to *https://api.whoisfreaks.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**dnsBulk**](DnsApi.md#dnsBulk) | **POST** /v2.0/dns/bulk/live | Bulk DNS Lookup |
| [**dnsHistorical**](DnsApi.md#dnsHistorical) | **GET** /v2.0/dns/historical | Historical DNS Lookup |
| [**dnsLive**](DnsApi.md#dnsLive) | **GET** /v2.0/dns/live | Live DNS Lookup |
| [**dnsReverse**](DnsApi.md#dnsReverse) | **GET** /v2.1/dns/reverse | Reverse DNS Lookup |


<a id="dnsBulk"></a>
# **dnsBulk**
> BulkDnsResponse dnsBulk(type, dnsBulkRequest, format)

Bulk DNS Lookup

Up to 100 domains + 100 IPs in one request.

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.DnsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DnsApi apiInstance = new DnsApi(defaultClient);
    String type = "all"; // String | 
    DnsBulkRequest dnsBulkRequest = new DnsBulkRequest(); // DnsBulkRequest | 
    String format = "json"; // String | 
    try {
      BulkDnsResponse result = apiInstance.dnsBulk(type, dnsBulkRequest, format);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DnsApi#dnsBulk");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **type** | **String**|  | [default to all] |
| **dnsBulkRequest** | [**DnsBulkRequest**](DnsBulkRequest.md)|  | |
| **format** | **String**|  | [optional] [default to json] [enum: json, xml] |

### Return type

[**BulkDnsResponse**](BulkDnsResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |
| **4XX** | Error response (4XX) |  -  |

<a id="dnsHistorical"></a>
# **dnsHistorical**
> HistoricalDnsResponse dnsHistorical(domainName, type, page, format)

Historical DNS Lookup

All historical DNS records. 2 credits per page (100 records/page).

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.DnsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DnsApi apiInstance = new DnsApi(defaultClient);
    String domainName = "domainName_example"; // String | 
    String type = "all"; // String | 
    Integer page = 1; // Integer | 
    String format = "json"; // String | 
    try {
      HistoricalDnsResponse result = apiInstance.dnsHistorical(domainName, type, page, format);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DnsApi#dnsHistorical");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **domainName** | **String**|  | |
| **type** | **String**|  | [default to all] |
| **page** | **Integer**|  | [optional] [default to 1] |
| **format** | **String**|  | [optional] [default to json] [enum: json, xml] |

### Return type

[**HistoricalDnsResponse**](HistoricalDnsResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |
| **4XX** | Error response (4XX) |  -  |

<a id="dnsLive"></a>
# **dnsLive**
> DnsResponse dnsLive(type, domainName, ipAddress, format)

Live DNS Lookup

Real-time DNS record lookup. 1 credit per query.

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.DnsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DnsApi apiInstance = new DnsApi(defaultClient);
    String type = "all"; // String | all or comma-separated: A,MX,NS,TXT,SOA,SPF,AAAA,CNAME
    String domainName = "domainName_example"; // String | 
    String ipAddress = "ipAddress_example"; // String | Use for PTR lookups
    String format = "json"; // String | 
    try {
      DnsResponse result = apiInstance.dnsLive(type, domainName, ipAddress, format);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DnsApi#dnsLive");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **type** | **String**| all or comma-separated: A,MX,NS,TXT,SOA,SPF,AAAA,CNAME | [default to all] |
| **domainName** | **String**|  | [optional] |
| **ipAddress** | **String**| Use for PTR lookups | [optional] |
| **format** | **String**|  | [optional] [default to json] [enum: json, xml] |

### Return type

[**DnsResponse**](DnsResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |
| **401** | Invalid API key |  -  |
| **429** | Too many requests |  -  |

<a id="dnsReverse"></a>
# **dnsReverse**
> ReverseDnsResponse dnsReverse(value, type, exact, page, format)

Reverse DNS Lookup

Search domains by IP or DNS value. 5 credits per page.

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.DnsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DnsApi apiInstance = new DnsApi(defaultClient);
    String value = "value_example"; // String | IP, CIDR, or record value
    String type = "a"; // String | 
    Boolean exact = true; // Boolean | 
    Integer page = 1; // Integer | 
    String format = "json"; // String | 
    try {
      ReverseDnsResponse result = apiInstance.dnsReverse(value, type, exact, page, format);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DnsApi#dnsReverse");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **value** | **String**| IP, CIDR, or record value | |
| **type** | **String**|  | [enum: a, mx, cname, ns, aaaa, txt, soa] |
| **exact** | **Boolean**|  | [optional] [default to true] |
| **page** | **Integer**|  | [optional] [default to 1] |
| **format** | **String**|  | [optional] [default to json] [enum: json, xml] |

### Return type

[**ReverseDnsResponse**](ReverseDnsResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |
| **4XX** | Error response (4XX) |  -  |

