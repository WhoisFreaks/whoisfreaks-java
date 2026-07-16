# GeolocationApi

All URIs are relative to *https://api.whoisfreaks.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**bulkGeolocation**](GeolocationApi.md#bulkGeolocation) | **POST** /v1.0/geolocation | Bulk IP Geolocation |
| [**geolocation**](GeolocationApi.md#geolocation) | **GET** /v1.0/geolocation | IP Geolocation Lookup |


<a id="bulkGeolocation"></a>
# **bulkGeolocation**
> List&lt;GeolocationResponse&gt; bulkGeolocation(bulkGeolocationRequest)

Bulk IP Geolocation

Up to 100 IPs.

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.GeolocationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GeolocationApi apiInstance = new GeolocationApi(defaultClient);
    BulkGeolocationRequest bulkGeolocationRequest = new BulkGeolocationRequest(); // BulkGeolocationRequest | 
    try {
      List<GeolocationResponse> result = apiInstance.bulkGeolocation(bulkGeolocationRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GeolocationApi#bulkGeolocation");
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
| **bulkGeolocationRequest** | [**BulkGeolocationRequest**](BulkGeolocationRequest.md)|  | |

### Return type

[**List&lt;GeolocationResponse&gt;**](GeolocationResponse.md)

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

<a id="geolocation"></a>
# **geolocation**
> GeolocationResponse geolocation(ip)

IP Geolocation Lookup

Get location, ASN, currency for an IP. 1 credit.

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.GeolocationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GeolocationApi apiInstance = new GeolocationApi(defaultClient);
    String ip = "ip_example"; // String | 
    try {
      GeolocationResponse result = apiInstance.geolocation(ip);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GeolocationApi#geolocation");
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

### Return type

[**GeolocationResponse**](GeolocationResponse.md)

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

