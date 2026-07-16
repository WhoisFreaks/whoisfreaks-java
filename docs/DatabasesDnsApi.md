# DatabasesDnsApi

All URIs are relative to *https://api.whoisfreaks.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**dbDnsDaily**](DatabasesDnsApi.md#dbDnsDaily) | **GET** /v3.2/download/dbupdate/daily/dns | DNS Database Daily |
| [**dbDnsMonthly**](DatabasesDnsApi.md#dbDnsMonthly) | **GET** /v3.2/download/dbupdate/monthly/dns | DNS Database Monthly |
| [**dbDnsWeekly**](DatabasesDnsApi.md#dbDnsWeekly) | **GET** /v3.2/download/dbupdate/weekly/dns | DNS Database Weekly |


<a id="dbDnsDaily"></a>
# **dbDnsDaily**
> File dbDnsDaily(date)

DNS Database Daily

DNS Database Daily. Returns the file/snapshot described by this operation.

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.DatabasesDnsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DatabasesDnsApi apiInstance = new DatabasesDnsApi(defaultClient);
    LocalDate date = LocalDate.now(); // LocalDate | yyyy-MM-dd; omit for latest
    try {
      File result = apiInstance.dbDnsDaily(date);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatabasesDnsApi#dbDnsDaily");
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

<a id="dbDnsMonthly"></a>
# **dbDnsMonthly**
> File dbDnsMonthly(date)

DNS Database Monthly

DNS Database Monthly. Returns the file/snapshot described by this operation.

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.DatabasesDnsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DatabasesDnsApi apiInstance = new DatabasesDnsApi(defaultClient);
    LocalDate date = LocalDate.now(); // LocalDate | yyyy-MM-dd; omit for latest
    try {
      File result = apiInstance.dbDnsMonthly(date);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatabasesDnsApi#dbDnsMonthly");
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

<a id="dbDnsWeekly"></a>
# **dbDnsWeekly**
> File dbDnsWeekly(date)

DNS Database Weekly

DNS Database Weekly. Returns the file/snapshot described by this operation.

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.DatabasesDnsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DatabasesDnsApi apiInstance = new DatabasesDnsApi(defaultClient);
    LocalDate date = LocalDate.now(); // LocalDate | yyyy-MM-dd; omit for latest
    try {
      File result = apiInstance.dbDnsWeekly(date);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatabasesDnsApi#dbDnsWeekly");
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

