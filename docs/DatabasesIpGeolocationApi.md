# DatabasesIpGeolocationApi

All URIs are relative to *https://api.whoisfreaks.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**dbIpCity**](DatabasesIpGeolocationApi.md#dbIpCity) | **GET** /v3.3/download/snapshot/ip/city | IP to City Snapshot |
| [**dbIpCityStatus**](DatabasesIpGeolocationApi.md#dbIpCityStatus) | **GET** /v3.3/status/snapshot/ip/city | IP to City Snapshot Status |
| [**dbIpCountry**](DatabasesIpGeolocationApi.md#dbIpCountry) | **GET** /v3.3/download/snapshot/ip/country | IP to Country Snapshot |
| [**dbIpCountryStatus**](DatabasesIpGeolocationApi.md#dbIpCountryStatus) | **GET** /v3.3/status/snapshot/ip/country | IP to Country Snapshot Status |


<a id="dbIpCity"></a>
# **dbIpCity**
> File dbIpCity(date)

IP to City Snapshot

IP to City Snapshot. Returns the file/snapshot described by this operation.

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.DatabasesIpGeolocationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DatabasesIpGeolocationApi apiInstance = new DatabasesIpGeolocationApi(defaultClient);
    LocalDate date = LocalDate.now(); // LocalDate | 
    try {
      File result = apiInstance.dbIpCity(date);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatabasesIpGeolocationApi#dbIpCity");
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
| **200** | ZIP archive |  -  |
| **4XX** | Error response (4XX) |  -  |

<a id="dbIpCityStatus"></a>
# **dbIpCityStatus**
> SnapshotStatus dbIpCityStatus()

IP to City Snapshot Status

IP to City Snapshot Status. Returns the file/snapshot described by this operation.

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.DatabasesIpGeolocationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DatabasesIpGeolocationApi apiInstance = new DatabasesIpGeolocationApi(defaultClient);
    try {
      SnapshotStatus result = apiInstance.dbIpCityStatus();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatabasesIpGeolocationApi#dbIpCityStatus");
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

<a id="dbIpCountry"></a>
# **dbIpCountry**
> File dbIpCountry(date)

IP to Country Snapshot

IP to Country Snapshot. Returns the file/snapshot described by this operation.

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.DatabasesIpGeolocationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DatabasesIpGeolocationApi apiInstance = new DatabasesIpGeolocationApi(defaultClient);
    LocalDate date = LocalDate.now(); // LocalDate | 
    try {
      File result = apiInstance.dbIpCountry(date);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatabasesIpGeolocationApi#dbIpCountry");
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
| **200** | ZIP archive |  -  |
| **4XX** | Error response (4XX) |  -  |

<a id="dbIpCountryStatus"></a>
# **dbIpCountryStatus**
> SnapshotStatus dbIpCountryStatus()

IP to Country Snapshot Status

IP to Country Snapshot Status. Returns the file/snapshot described by this operation.

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.DatabasesIpGeolocationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DatabasesIpGeolocationApi apiInstance = new DatabasesIpGeolocationApi(defaultClient);
    try {
      SnapshotStatus result = apiInstance.dbIpCountryStatus();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatabasesIpGeolocationApi#dbIpCountryStatus");
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

