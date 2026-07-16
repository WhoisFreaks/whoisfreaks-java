# WhoisApi

All URIs are relative to *https://api.whoisfreaks.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**bulkWhois**](WhoisApi.md#bulkWhois) | **POST** /v2.0/bulkwhois/live | Bulk WHOIS Lookup |
| [**whoisHistory**](WhoisApi.md#whoisHistory) | **GET** /v2.0/whois/history | Historical WHOIS records for a domain |
| [**whoisLive**](WhoisApi.md#whoisLive) | **GET** /v2.0/whois/live | Live WHOIS Lookup |
| [**whoisReverse**](WhoisApi.md#whoisReverse) | **GET** /v2.0/whois/reverse | Reverse WHOIS lookup by keyword |


<a id="bulkWhois"></a>
# **bulkWhois**
> BulkWhoisResponse bulkWhois(bulkWhoisRequest, format)

Bulk WHOIS Lookup

Up to 100 domains in one request. 1 credit per successful domain.

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.WhoisApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    WhoisApi apiInstance = new WhoisApi(defaultClient);
    BulkWhoisRequest bulkWhoisRequest = new BulkWhoisRequest(); // BulkWhoisRequest | 
    String format = "json"; // String | 
    try {
      BulkWhoisResponse result = apiInstance.bulkWhois(bulkWhoisRequest, format);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WhoisApi#bulkWhois");
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
| **bulkWhoisRequest** | [**BulkWhoisRequest**](BulkWhoisRequest.md)|  | |
| **format** | **String**|  | [optional] [default to json] [enum: json, xml] |

### Return type

[**BulkWhoisResponse**](BulkWhoisResponse.md)

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

<a id="whoisHistory"></a>
# **whoisHistory**
> WhoisHistoricalResponse whoisHistory(domainName, page, format)

Historical WHOIS records for a domain

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.WhoisApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    WhoisApi apiInstance = new WhoisApi(defaultClient);
    String domainName = "domainName_example"; // String | Domain to fetch historical WHOIS records for
    Integer page = 56; // Integer | Page number
    String format = "json"; // String | 
    try {
      WhoisHistoricalResponse result = apiInstance.whoisHistory(domainName, page, format);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WhoisApi#whoisHistory");
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
| **domainName** | **String**| Domain to fetch historical WHOIS records for | |
| **page** | **Integer**| Page number | [optional] |
| **format** | **String**|  | [optional] [enum: json, xml] |

### Return type

[**WhoisHistoricalResponse**](WhoisHistoricalResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Historical WHOIS records |  -  |

<a id="whoisLive"></a>
# **whoisLive**
> WhoisResponse whoisLive(domainName, format)

Live WHOIS Lookup

Real-time WHOIS lookup from authoritative servers. Cost 1 credit.

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.WhoisApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    WhoisApi apiInstance = new WhoisApi(defaultClient);
    String domainName = "whoisfreaks.com"; // String | 
    String format = "json"; // String | 
    try {
      WhoisResponse result = apiInstance.whoisLive(domainName, format);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WhoisApi#whoisLive");
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
| **format** | **String**|  | [optional] [default to json] [enum: json, xml] |

### Return type

[**WhoisResponse**](WhoisResponse.md)

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
| **404** | Not found |  -  |
| **429** | Too many requests |  -  |

<a id="whoisReverse"></a>
# **whoisReverse**
> ReverseWhoisResponse whoisReverse(keyword, page, format)

Reverse WHOIS lookup by keyword

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.WhoisApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    WhoisApi apiInstance = new WhoisApi(defaultClient);
    String keyword = "keyword_example"; // String | Keyword to search across WHOIS records
    Integer page = 56; // Integer | Page number
    String format = "json"; // String | 
    try {
      ReverseWhoisResponse result = apiInstance.whoisReverse(keyword, page, format);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WhoisApi#whoisReverse");
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
| **keyword** | **String**| Keyword to search across WHOIS records | |
| **page** | **Integer**| Page number | [optional] |
| **format** | **String**|  | [optional] [enum: json, xml] |

### Return type

[**ReverseWhoisResponse**](ReverseWhoisResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Reverse WHOIS results (paginated) |  -  |

