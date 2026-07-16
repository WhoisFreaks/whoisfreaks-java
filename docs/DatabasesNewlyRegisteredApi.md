# DatabasesNewlyRegisteredApi

All URIs are relative to *https://api.whoisfreaks.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**dbNewlyCctld**](DatabasesNewlyRegisteredApi.md#dbNewlyCctld) | **GET** /v3.1/download/domainer/cctld | Newly Registered ccTLD (CSV) |
| [**dbNewlyCctldCleaned**](DatabasesNewlyRegisteredApi.md#dbNewlyCctldCleaned) | **GET** /v3.1/download/domainer/cctld/cleaned | Newly Registered ccTLD Cleaned WHOIS (CSV) |
| [**dbNewlyCctldJson**](DatabasesNewlyRegisteredApi.md#dbNewlyCctldJson) | **GET** /v3.1/domains/newly/cctld | Newly Registered ccTLD (JSON) |
| [**dbNewlyDns**](DatabasesNewlyRegisteredApi.md#dbNewlyDns) | **GET** /v3.1/download/domainer/newly/dns | Newly Registered With DNS |
| [**dbNewlyGtld**](DatabasesNewlyRegisteredApi.md#dbNewlyGtld) | **GET** /v3.1/download/domainer/gtld | Newly Registered gTLD (CSV) |
| [**dbNewlyGtldCleaned**](DatabasesNewlyRegisteredApi.md#dbNewlyGtldCleaned) | **GET** /v3.1/download/domainer/gtld/cleaned | Newly Registered gTLD Cleaned WHOIS (CSV) |
| [**dbNewlyGtldJson**](DatabasesNewlyRegisteredApi.md#dbNewlyGtldJson) | **GET** /v3.1/domains/newly/gtld | Newly Registered gTLD (JSON) |


<a id="dbNewlyCctld"></a>
# **dbNewlyCctld**
> File dbNewlyCctld(whois, date, tlds)

Newly Registered ccTLD (CSV)

Newly Registered ccTLD (CSV). Returns the file/snapshot described by this operation.

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.DatabasesNewlyRegisteredApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DatabasesNewlyRegisteredApi apiInstance = new DatabasesNewlyRegisteredApi(defaultClient);
    Boolean whois = true; // Boolean | 
    LocalDate date = LocalDate.now(); // LocalDate | yyyy-MM-dd; omit for latest
    String tlds = "tlds_example"; // String | 
    try {
      File result = apiInstance.dbNewlyCctld(whois, date, tlds);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatabasesNewlyRegisteredApi#dbNewlyCctld");
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
| **tlds** | **String**|  | [optional] |

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

<a id="dbNewlyCctldCleaned"></a>
# **dbNewlyCctldCleaned**
> File dbNewlyCctldCleaned(date)

Newly Registered ccTLD Cleaned WHOIS (CSV)

Newly Registered ccTLD Cleaned WHOIS (CSV). Returns the file/snapshot described by this operation.

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.DatabasesNewlyRegisteredApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DatabasesNewlyRegisteredApi apiInstance = new DatabasesNewlyRegisteredApi(defaultClient);
    LocalDate date = LocalDate.now(); // LocalDate | yyyy-MM-dd; omit for latest
    try {
      File result = apiInstance.dbNewlyCctldCleaned(date);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatabasesNewlyRegisteredApi#dbNewlyCctldCleaned");
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

<a id="dbNewlyCctldJson"></a>
# **dbNewlyCctldJson**
> List&lt;String&gt; dbNewlyCctldJson(date, tlds)

Newly Registered ccTLD (JSON)

Newly Registered ccTLD (JSON). Returns the file/snapshot described by this operation.

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.DatabasesNewlyRegisteredApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DatabasesNewlyRegisteredApi apiInstance = new DatabasesNewlyRegisteredApi(defaultClient);
    LocalDate date = LocalDate.now(); // LocalDate | yyyy-MM-dd; omit for latest
    String tlds = "tlds_example"; // String | 
    try {
      List<String> result = apiInstance.dbNewlyCctldJson(date, tlds);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatabasesNewlyRegisteredApi#dbNewlyCctldJson");
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

<a id="dbNewlyDns"></a>
# **dbNewlyDns**
> File dbNewlyDns(date)

Newly Registered With DNS

Newly Registered With DNS. Returns the file/snapshot described by this operation.

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.DatabasesNewlyRegisteredApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DatabasesNewlyRegisteredApi apiInstance = new DatabasesNewlyRegisteredApi(defaultClient);
    LocalDate date = LocalDate.now(); // LocalDate | yyyy-MM-dd; omit for latest
    try {
      File result = apiInstance.dbNewlyDns(date);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatabasesNewlyRegisteredApi#dbNewlyDns");
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
| **200** | JSON array of domains with DNS |  -  |
| **4XX** | Error response (4XX) |  -  |

<a id="dbNewlyGtld"></a>
# **dbNewlyGtld**
> File dbNewlyGtld(whois, date, tlds)

Newly Registered gTLD (CSV)

Newly Registered gTLD (CSV). Returns the file/snapshot described by this operation.

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.DatabasesNewlyRegisteredApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DatabasesNewlyRegisteredApi apiInstance = new DatabasesNewlyRegisteredApi(defaultClient);
    Boolean whois = true; // Boolean | 
    LocalDate date = LocalDate.now(); // LocalDate | yyyy-MM-dd; omit for latest
    String tlds = "tlds_example"; // String | 
    try {
      File result = apiInstance.dbNewlyGtld(whois, date, tlds);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatabasesNewlyRegisteredApi#dbNewlyGtld");
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
| **tlds** | **String**|  | [optional] |

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

<a id="dbNewlyGtldCleaned"></a>
# **dbNewlyGtldCleaned**
> File dbNewlyGtldCleaned(date)

Newly Registered gTLD Cleaned WHOIS (CSV)

Newly Registered gTLD Cleaned WHOIS (CSV). Returns the file/snapshot described by this operation.

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.DatabasesNewlyRegisteredApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DatabasesNewlyRegisteredApi apiInstance = new DatabasesNewlyRegisteredApi(defaultClient);
    LocalDate date = LocalDate.now(); // LocalDate | yyyy-MM-dd; omit for latest
    try {
      File result = apiInstance.dbNewlyGtldCleaned(date);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatabasesNewlyRegisteredApi#dbNewlyGtldCleaned");
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

<a id="dbNewlyGtldJson"></a>
# **dbNewlyGtldJson**
> List&lt;String&gt; dbNewlyGtldJson(date, tlds)

Newly Registered gTLD (JSON)

Newly Registered gTLD (JSON). Returns the file/snapshot described by this operation.

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.DatabasesNewlyRegisteredApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DatabasesNewlyRegisteredApi apiInstance = new DatabasesNewlyRegisteredApi(defaultClient);
    LocalDate date = LocalDate.now(); // LocalDate | yyyy-MM-dd; omit for latest
    String tlds = "tlds_example"; // String | 
    try {
      List<String> result = apiInstance.dbNewlyGtldJson(date, tlds);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatabasesNewlyRegisteredApi#dbNewlyGtldJson");
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

