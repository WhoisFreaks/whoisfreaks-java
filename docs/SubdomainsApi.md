# SubdomainsApi

All URIs are relative to *https://api.whoisfreaks.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**subdomains**](SubdomainsApi.md#subdomains) | **GET** /v1.0/subdomains | Subdomains Lookup |


<a id="subdomains"></a>
# **subdomains**
> SubdomainsResponse subdomains(domain, after, before, status, page, format)

Subdomains Lookup

All subdomains including nested. 2 credits per query.

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.SubdomainsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    SubdomainsApi apiInstance = new SubdomainsApi(defaultClient);
    String domain = "domain_example"; // String | 
    LocalDate after = LocalDate.now(); // LocalDate | 
    LocalDate before = LocalDate.now(); // LocalDate | 
    String status = "active"; // String | 
    Integer page = 1; // Integer | 
    String format = "json"; // String | 
    try {
      SubdomainsResponse result = apiInstance.subdomains(domain, after, before, status, page, format);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SubdomainsApi#subdomains");
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
| **domain** | **String**|  | |
| **after** | **LocalDate**|  | [optional] |
| **before** | **LocalDate**|  | [optional] |
| **status** | **String**|  | [optional] [enum: active, inactive] |
| **page** | **Integer**|  | [optional] [default to 1] |
| **format** | **String**|  | [optional] [default to json] [enum: json, xml] |

### Return type

[**SubdomainsResponse**](SubdomainsResponse.md)

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

