# DatabasesAsnWhoisApi

All URIs are relative to *https://api.whoisfreaks.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**dbAsnWhois**](DatabasesAsnWhoisApi.md#dbAsnWhois) | **GET** /v3.3/download/snapshot/asn/whois | ASN WHOIS Snapshot |
| [**dbAsnWhoisStatus**](DatabasesAsnWhoisApi.md#dbAsnWhoisStatus) | **GET** /v3.3/status/snapshot/asn/whois | ASN WHOIS Snapshot Status |


<a id="dbAsnWhois"></a>
# **dbAsnWhois**
> File dbAsnWhois(date)

ASN WHOIS Snapshot

ASN WHOIS Snapshot. Returns the file/snapshot described by this operation.

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.DatabasesAsnWhoisApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DatabasesAsnWhoisApi apiInstance = new DatabasesAsnWhoisApi(defaultClient);
    LocalDate date = LocalDate.now(); // LocalDate | 
    try {
      File result = apiInstance.dbAsnWhois(date);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatabasesAsnWhoisApi#dbAsnWhois");
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
| **date** | **LocalDate**|  | |

### Return type

[**File**](File.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/octet-stream, application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | JSON gzipped |  -  |
| **4XX** | Error response (4XX) |  -  |

<a id="dbAsnWhoisStatus"></a>
# **dbAsnWhoisStatus**
> SnapshotStatus dbAsnWhoisStatus()

ASN WHOIS Snapshot Status

ASN WHOIS Snapshot Status. Returns the file/snapshot described by this operation.

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.DatabasesAsnWhoisApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DatabasesAsnWhoisApi apiInstance = new DatabasesAsnWhoisApi(defaultClient);
    try {
      SnapshotStatus result = apiInstance.dbAsnWhoisStatus();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatabasesAsnWhoisApi#dbAsnWhoisStatus");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**SnapshotStatus**](SnapshotStatus.md)

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

