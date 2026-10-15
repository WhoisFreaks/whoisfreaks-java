# DatabasesWhoisApi

All URIs are relative to *https://api.whoisfreaks.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**dbWhoisDaily**](DatabasesWhoisApi.md#dbWhoisDaily) | **GET** /v3.3/download/dbupdate/daily/domains/whois | WHOIS Database Daily |
| [**dbWhoisMonthly**](DatabasesWhoisApi.md#dbWhoisMonthly) | **GET** /v3.3/download/dbupdate/monthly/domains/whois | WHOIS Database Monthly |
| [**dbWhoisWeekly**](DatabasesWhoisApi.md#dbWhoisWeekly) | **GET** /v3.3/download/dbupdate/weekly/domains/whois | WHOIS Database Weekly |


<a id="dbWhoisDaily"></a>
# **dbWhoisDaily**
> File dbWhoisDaily(date)

WHOIS Database Daily

WHOIS Database Daily. Returns the file/snapshot described by this operation.

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
import com.whoisfreaks.client.api.DatabasesWhoisApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DatabasesWhoisApi apiInstance = new DatabasesWhoisApi(defaultClient);
    LocalDate date = LocalDate.parse("2026-10-01"); // LocalDate | yyyy-MM-dd; omit for latest
    try {
      File result = apiInstance.dbWhoisDaily(date);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatabasesWhoisApi#dbWhoisDaily");
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

<a id="dbWhoisMonthly"></a>
# **dbWhoisMonthly**
> File dbWhoisMonthly(date)

WHOIS Database Monthly

WHOIS Database Monthly. Returns the file/snapshot described by this operation.

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
import com.whoisfreaks.client.api.DatabasesWhoisApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DatabasesWhoisApi apiInstance = new DatabasesWhoisApi(defaultClient);
    LocalDate date = LocalDate.parse("2026-10-01"); // LocalDate | yyyy-MM-dd; omit for latest
    try {
      File result = apiInstance.dbWhoisMonthly(date);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatabasesWhoisApi#dbWhoisMonthly");
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

<a id="dbWhoisWeekly"></a>
# **dbWhoisWeekly**
> File dbWhoisWeekly(date)

WHOIS Database Weekly

WHOIS Database Weekly. Returns the file/snapshot described by this operation.

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
import com.whoisfreaks.client.api.DatabasesWhoisApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DatabasesWhoisApi apiInstance = new DatabasesWhoisApi(defaultClient);
    LocalDate date = LocalDate.parse("2026-10-01"); // LocalDate | yyyy-MM-dd; omit for latest
    try {
      File result = apiInstance.dbWhoisWeekly(date);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatabasesWhoisApi#dbWhoisWeekly");
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

