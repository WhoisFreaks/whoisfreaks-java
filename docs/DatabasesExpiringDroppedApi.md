# DatabasesExpiringDroppedApi

All URIs are relative to *https://api.whoisfreaks.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**dbDropped**](DatabasesExpiringDroppedApi.md#dbDropped) | **GET** /v3.1/download/domainer/dropped | Dropped Domains |
| [**dbDroppedBacklinks**](DatabasesExpiringDroppedApi.md#dbDroppedBacklinks) | **GET** /v3.3/download/domainer/dropped/backlinks | Dropped With Backlinks |
| [**dbDroppedJson**](DatabasesExpiringDroppedApi.md#dbDroppedJson) | **GET** /v3.1/domains/dropped | Dropped Domains (JSON) |
| [**dbExpired**](DatabasesExpiringDroppedApi.md#dbExpired) | **GET** /v3.1/download/domainer/expired | Expiring Domains |
| [**dbExpiredCleaned**](DatabasesExpiringDroppedApi.md#dbExpiredCleaned) | **GET** /v3.1/download/domainer/expired/cleaned | Expiring Cleaned WHOIS |


<a id="dbDropped"></a>
# **dbDropped**
> File dbDropped(whois, date)

Dropped Domains

Dropped Domains. Returns the file/snapshot described by this operation.

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
import com.whoisfreaks.client.api.DatabasesExpiringDroppedApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DatabasesExpiringDroppedApi apiInstance = new DatabasesExpiringDroppedApi(defaultClient);
    Boolean whois = true; // Boolean | 
    LocalDate date = LocalDate.parse("2026-10-01"); // LocalDate | yyyy-MM-dd; omit for latest
    try {
      File result = apiInstance.dbDropped(whois, date);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatabasesExpiringDroppedApi#dbDropped");
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
| **whois** | **Boolean**|  | |
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

<a id="dbDroppedBacklinks"></a>
# **dbDroppedBacklinks**
> File dbDroppedBacklinks(whois, date)

Dropped With Backlinks

Dropped With Backlinks. Returns the file/snapshot described by this operation.

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
import com.whoisfreaks.client.api.DatabasesExpiringDroppedApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DatabasesExpiringDroppedApi apiInstance = new DatabasesExpiringDroppedApi(defaultClient);
    Boolean whois = true; // Boolean | 
    LocalDate date = LocalDate.parse("2026-10-01"); // LocalDate | yyyy-MM-dd; omit for latest
    try {
      File result = apiInstance.dbDroppedBacklinks(whois, date);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatabasesExpiringDroppedApi#dbDroppedBacklinks");
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
| **whois** | **Boolean**|  | [optional] |
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

<a id="dbDroppedJson"></a>
# **dbDroppedJson**
> List&lt;String&gt; dbDroppedJson(date, tlds)

Dropped Domains (JSON)

Dropped Domains (JSON). Returns the file/snapshot described by this operation.

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
import com.whoisfreaks.client.api.DatabasesExpiringDroppedApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DatabasesExpiringDroppedApi apiInstance = new DatabasesExpiringDroppedApi(defaultClient);
    LocalDate date = LocalDate.parse("2026-10-01"); // LocalDate | yyyy-MM-dd; omit for latest
    String tlds = "com,net"; // String | 
    try {
      List<String> result = apiInstance.dbDroppedJson(date, tlds);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatabasesExpiringDroppedApi#dbDroppedJson");
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
| **tlds** | **String**|  | [optional] |

### Return type

**List&lt;String&gt;**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | JSON array of domains |  -  |
| **4XX** | Error response (4XX) |  -  |

<a id="dbExpired"></a>
# **dbExpired**
> File dbExpired(whois, date)

Expiring Domains

Expiring Domains. Returns the file/snapshot described by this operation.

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
import com.whoisfreaks.client.api.DatabasesExpiringDroppedApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DatabasesExpiringDroppedApi apiInstance = new DatabasesExpiringDroppedApi(defaultClient);
    Boolean whois = true; // Boolean | 
    LocalDate date = LocalDate.parse("2026-10-01"); // LocalDate | yyyy-MM-dd; omit for latest
    try {
      File result = apiInstance.dbExpired(whois, date);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatabasesExpiringDroppedApi#dbExpired");
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
| **whois** | **Boolean**|  | |
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

<a id="dbExpiredCleaned"></a>
# **dbExpiredCleaned**
> File dbExpiredCleaned(date)

Expiring Cleaned WHOIS

Expiring Cleaned WHOIS. Returns the file/snapshot described by this operation.

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
import com.whoisfreaks.client.api.DatabasesExpiringDroppedApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DatabasesExpiringDroppedApi apiInstance = new DatabasesExpiringDroppedApi(defaultClient);
    LocalDate date = LocalDate.parse("2026-10-01"); // LocalDate | yyyy-MM-dd; omit for latest
    try {
      File result = apiInstance.dbExpiredCleaned(date);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatabasesExpiringDroppedApi#dbExpiredCleaned");
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

