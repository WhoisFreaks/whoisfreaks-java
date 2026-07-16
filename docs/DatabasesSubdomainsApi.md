# DatabasesSubdomainsApi

All URIs are relative to *https://api.whoisfreaks.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**dbSubdomainsDaily**](DatabasesSubdomainsApi.md#dbSubdomainsDaily) | **GET** /v3.2/download/dbupdate/daily/subdomains | Subdomains Daily |
| [**dbSubdomainsMonthly**](DatabasesSubdomainsApi.md#dbSubdomainsMonthly) | **GET** /v3.2/download/dbupdate/monthly/subdomains | Subdomains Monthly |
| [**dbSubdomainsWeekly**](DatabasesSubdomainsApi.md#dbSubdomainsWeekly) | **GET** /v3.2/download/dbupdate/weekly/subdomains | Subdomains Weekly |


<a id="dbSubdomainsDaily"></a>
# **dbSubdomainsDaily**
> File dbSubdomainsDaily(date)

Subdomains Daily

Subdomains Daily. Returns the file/snapshot described by this operation.

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.DatabasesSubdomainsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DatabasesSubdomainsApi apiInstance = new DatabasesSubdomainsApi(defaultClient);
    LocalDate date = LocalDate.now(); // LocalDate | yyyy-MM-dd; omit for latest
    try {
      File result = apiInstance.dbSubdomainsDaily(date);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatabasesSubdomainsApi#dbSubdomainsDaily");
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
| **date** | **LocalDate**| yyyy-MM-dd; omit for latest | [optional] |

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
| **200** | CSV |  -  |
| **4XX** | Error response (4XX) |  -  |

<a id="dbSubdomainsMonthly"></a>
# **dbSubdomainsMonthly**
> File dbSubdomainsMonthly(date)

Subdomains Monthly

Subdomains Monthly. Returns the file/snapshot described by this operation.

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.DatabasesSubdomainsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DatabasesSubdomainsApi apiInstance = new DatabasesSubdomainsApi(defaultClient);
    LocalDate date = LocalDate.now(); // LocalDate | yyyy-MM-dd; omit for latest
    try {
      File result = apiInstance.dbSubdomainsMonthly(date);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatabasesSubdomainsApi#dbSubdomainsMonthly");
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
| **date** | **LocalDate**| yyyy-MM-dd; omit for latest | [optional] |

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
| **200** | CSV |  -  |
| **4XX** | Error response (4XX) |  -  |

<a id="dbSubdomainsWeekly"></a>
# **dbSubdomainsWeekly**
> File dbSubdomainsWeekly(date)

Subdomains Weekly

Subdomains Weekly. Returns the file/snapshot described by this operation.

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.DatabasesSubdomainsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DatabasesSubdomainsApi apiInstance = new DatabasesSubdomainsApi(defaultClient);
    LocalDate date = LocalDate.now(); // LocalDate | yyyy-MM-dd; omit for latest
    try {
      File result = apiInstance.dbSubdomainsWeekly(date);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatabasesSubdomainsApi#dbSubdomainsWeekly");
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
| **date** | **LocalDate**| yyyy-MM-dd; omit for latest | [optional] |

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
| **200** | CSV |  -  |
| **4XX** | Error response (4XX) |  -  |

