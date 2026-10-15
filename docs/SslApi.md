# SslApi

All URIs are relative to *https://api.whoisfreaks.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**sslLookup**](SslApi.md#sslLookup) | **GET** /v1.0/ssl/live | SSL Certificate Lookup |


<a id="sslLookup"></a>
# **sslLookup**
> SslResponse sslLookup(domainName, chain, sslRaw, format)

SSL Certificate Lookup

Real-time SSL cert with optional chain.

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.model.*;
import java.io.File;
import java.time.LocalDate;
import java.util.List;
import com.whoisfreaks.client.api.SslApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    SslApi apiInstance = new SslApi(defaultClient);
    String domainName = "whoisfreaks.com"; // String | 
    Boolean chain = false; // Boolean | 
    Boolean sslRaw = false; // Boolean | 
    String format = "json"; // String | 
    try {
      SslResponse result = apiInstance.sslLookup(domainName, chain, sslRaw, format);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SslApi#sslLookup");
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
| **chain** | **Boolean**|  | [optional] [default to false] |
| **sslRaw** | **Boolean**|  | [optional] [default to false] |
| **format** | **String**|  | [optional] [default to json] [enum: json, xml] |

### Return type

[**SslResponse**](SslResponse.md)

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

