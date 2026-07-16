# TyposquattingApi

All URIs are relative to *https://api.whoisfreaks.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**typosquatting**](TyposquattingApi.md#typosquatting) | **GET** /v3.0/domain/typos | Typosquatting Lookup |


<a id="typosquatting"></a>
# **typosquatting**
> TyposquattingResponse typosquatting(keyword, pattern, pageToken)

Typosquatting Lookup

Find typo variants of a brand. 5 credits per page.

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.TyposquattingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TyposquattingApi apiInstance = new TyposquattingApi(defaultClient);
    String keyword = "keyword_example"; // String | 
    String pattern = "pattern_example"; // String | 
    String pageToken = "pageToken_example"; // String | 
    try {
      TyposquattingResponse result = apiInstance.typosquatting(keyword, pattern, pageToken);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TyposquattingApi#typosquatting");
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
| **keyword** | **String**|  | [optional] |
| **pattern** | **String**|  | [optional] |
| **pageToken** | **String**|  | [optional] |

### Return type

[**TyposquattingResponse**](TyposquattingResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |
| **400** | Bad request |  -  |
| **401** | Invalid API key |  -  |

