# IpWhoisApi

All URIs are relative to *https://api.whoisfreaks.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**ipWhois**](IpWhoisApi.md#ipWhois) | **GET** /v1.0/ip-whois | IP WHOIS Lookup |


<a id="ipWhois"></a>
# **ipWhois**
> IpWhoisResponse ipWhois(ip, format)

IP WHOIS Lookup

WHOIS for an IP address. 1 credit.

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.IpWhoisApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    IpWhoisApi apiInstance = new IpWhoisApi(defaultClient);
    String ip = "ip_example"; // String | 
    String format = "json"; // String | 
    try {
      IpWhoisResponse result = apiInstance.ipWhois(ip, format);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling IpWhoisApi#ipWhois");
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
| **ip** | **String**|  | |
| **format** | **String**|  | [optional] [default to json] [enum: json, xml] |

### Return type

[**IpWhoisResponse**](IpWhoisResponse.md)

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

