# AccountApi

All URIs are relative to *https://api.whoisfreaks.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**accountUsage**](AccountApi.md#accountUsage) | **GET** /v1.0/whoisapi/usage | Account Usage |
| [**databaseFileStatus**](AccountApi.md#databaseFileStatus) | **GET** /v3.3/status | Database File Status (Public) |
| [**rotateApiKey**](AccountApi.md#rotateApiKey) | **GET** /v1.0/api-key/rotate | Rotate API Key |


<a id="accountUsage"></a>
# **accountUsage**
> AccountUsageResponse accountUsage()

Account Usage

Account Usage. Returns the file/snapshot described by this operation.

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.AccountApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AccountApi apiInstance = new AccountApi(defaultClient);
    try {
      AccountUsageResponse result = apiInstance.accountUsage();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AccountApi#accountUsage");
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

[**AccountUsageResponse**](AccountUsageResponse.md)

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

<a id="databaseFileStatus"></a>
# **databaseFileStatus**
> DatabaseFileStatus databaseFileStatus()

Database File Status (Public)

No API key required. Returns freshness of all downloadable files.

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.AccountApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");

    AccountApi apiInstance = new AccountApi(defaultClient);
    try {
      DatabaseFileStatus result = apiInstance.databaseFileStatus();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AccountApi#databaseFileStatus");
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

[**DatabaseFileStatus**](DatabaseFileStatus.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |
| **429** | Too many requests |  -  |

<a id="rotateApiKey"></a>
# **rotateApiKey**
> String rotateApiKey()

Rotate API Key

Rotate API Key. Returns the file/snapshot described by this operation.

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.AccountApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AccountApi apiInstance = new AccountApi(defaultClient);
    try {
      String result = apiInstance.rotateApiKey();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AccountApi#rotateApiKey");
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

**String**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Key rotated |  -  |
| **401** | Not allowed |  -  |

