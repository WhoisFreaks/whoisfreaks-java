# DomainReputationApi

All URIs are relative to *https://api.whoisfreaks.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**domainReputation**](DomainReputationApi.md#domainReputation) | **GET** /v1/domain/security | Domain Reputation Lookup |


<a id="domainReputation"></a>
# **domainReputation**
> DomainReputationResponse domainReputation(domainName, format)

Domain Reputation Lookup

Real-time domain threat assessment. Returns risk verdict, trust score, DGA analysis, threat intelligence matches, and security signals. 1 credit.

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
import com.whoisfreaks.client.api.DomainReputationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DomainReputationApi apiInstance = new DomainReputationApi(defaultClient);
    String domainName = "amazon.com"; // String | The domain name to assess
    String format = "json"; // String | 
    try {
      DomainReputationResponse result = apiInstance.domainReputation(domainName, format);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DomainReputationApi#domainReputation");
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
| **domainName** | **String**| The domain name to assess | |
| **format** | **String**|  | [optional] [default to json] [enum: json, xml] |

### Return type

[**DomainReputationResponse**](DomainReputationResponse.md)

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
| **404** | Not found |  -  |
| **429** | Too many requests |  -  |

