# IpReputationApi

All URIs are relative to *https://api.whoisfreaks.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**bulkIpReputation**](IpReputationApi.md#bulkIpReputation) | **POST** /v1.0/security | Bulk IP Reputation |
| [**ipReputation**](IpReputationApi.md#ipReputation) | **GET** /v1.0/security | IP Reputation Lookup |


<a id="bulkIpReputation"></a>
# **bulkIpReputation**
> List&lt;IpReputationResponse&gt; bulkIpReputation(bulkGeolocationRequest)

Bulk IP Reputation

Up to 100 IPs.

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
import com.whoisfreaks.client.api.IpReputationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    IpReputationApi apiInstance = new IpReputationApi(defaultClient);
    BulkGeolocationRequest bulkGeolocationRequest = new BulkGeolocationRequest(); // BulkGeolocationRequest | 
    try {
      List<IpReputationResponse> result = apiInstance.bulkIpReputation(bulkGeolocationRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling IpReputationApi#bulkIpReputation");
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

[**List&lt;IpReputationResponse&gt;**](IpReputationResponse.md)

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

<a id="ipReputation"></a>
# **ipReputation**
> IpReputationResponse ipReputation(ip)

IP Reputation Lookup

Threat intel for IP: VPN, proxy, Tor, bots. 1 credit.

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
import com.whoisfreaks.client.api.IpReputationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    IpReputationApi apiInstance = new IpReputationApi(defaultClient);
    String ip = "8.8.8.8"; // String | 
    try {
      IpReputationResponse result = apiInstance.ipReputation(ip);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling IpReputationApi#ipReputation");
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

[**IpReputationResponse**](IpReputationResponse.md)

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

