# DomainAvailabilityApi

All URIs are relative to *https://api.whoisfreaks.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**bulkDomainAvailabilityV2**](DomainAvailabilityApi.md#bulkDomainAvailabilityV2) | **POST** /v2.0/domain/availability | Bulk Domain Availability Check |
| [**domainAvailabilityV2**](DomainAvailabilityApi.md#domainAvailabilityV2) | **GET** /v2.0/domain/availability | Domain Availability Check with Suggestions |


<a id="bulkDomainAvailabilityV2"></a>
# **bulkDomainAvailabilityV2**
> BulkDomainAvailabilityResponse bulkDomainAvailabilityV2(bulkDomainAvailabilityRequest, domain, format)

Bulk Domain Availability Check

Two bulk modes. Mode 1: POST domainNames array. Mode 2: POST tld array plus domain query param. Max 100 domains per request. 1 credit per domain checked.

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
import com.whoisfreaks.client.api.DomainAvailabilityApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DomainAvailabilityApi apiInstance = new DomainAvailabilityApi(defaultClient);
    BulkDomainAvailabilityRequest bulkDomainAvailabilityRequest = new BulkDomainAvailabilityRequest(); // BulkDomainAvailabilityRequest | 
    String domain = "google.com"; // String | Required for TLD-mode bulk check (base domain).
    String format = "json"; // String | 
    try {
      BulkDomainAvailabilityResponse result = apiInstance.bulkDomainAvailabilityV2(bulkDomainAvailabilityRequest, domain, format);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DomainAvailabilityApi#bulkDomainAvailabilityV2");
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
| **bulkDomainAvailabilityRequest** | [**BulkDomainAvailabilityRequest**](BulkDomainAvailabilityRequest.md)|  | |
| **domain** | **String**| Required for TLD-mode bulk check (base domain). | [optional] |
| **format** | **String**|  | [optional] [default to json] [enum: json, xml] |

### Return type

[**BulkDomainAvailabilityResponse**](BulkDomainAvailabilityResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |
| **400** | Bad request |  -  |
| **401** | Invalid API key |  -  |
| **429** | Too many requests |  -  |

<a id="domainAvailabilityV2"></a>
# **domainAvailabilityV2**
> DomainAvailabilityResponse domainAvailabilityV2(domain, sug, count, format)

Domain Availability Check with Suggestions

Check availability of a single domain and optionally get suggestions across multiple TLDs. 1 credit per domain checked. sug&#x3D;false checks only the queried domain; sug&#x3D;true returns up to &#x60;count&#x60; (max 100) TLD suggestions.

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
import com.whoisfreaks.client.api.DomainAvailabilityApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DomainAvailabilityApi apiInstance = new DomainAvailabilityApi(defaultClient);
    String domain = "google.com"; // String | The domain name to check
    Boolean sug = false; // Boolean | Whether to return TLD suggestions alongside the queried domain.
    Integer count = 5; // Integer | Number of TLD suggestions to return when sug=true. Maximum is 100.
    String format = "json"; // String | 
    try {
      DomainAvailabilityResponse result = apiInstance.domainAvailabilityV2(domain, sug, count, format);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DomainAvailabilityApi#domainAvailabilityV2");
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
| **domain** | **String**| The domain name to check | |
| **sug** | **Boolean**| Whether to return TLD suggestions alongside the queried domain. | [optional] [default to false] |
| **count** | **Integer**| Number of TLD suggestions to return when sug&#x3D;true. Maximum is 100. | [optional] [default to 5] |
| **format** | **String**|  | [optional] [default to json] [enum: json, xml] |

### Return type

[**DomainAvailabilityResponse**](DomainAvailabilityResponse.md)

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
| **429** | Too many requests |  -  |

