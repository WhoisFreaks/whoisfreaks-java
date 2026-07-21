# DatabasesThreatFeedApi

All URIs are relative to *https://api.whoisfreaks.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**downloadThreatFeedMalware**](DatabasesThreatFeedApi.md#downloadThreatFeedMalware) | **GET** /v3.4/download/threat-feed/malware | Download the daily malware threat feed (CSV) |
| [**downloadThreatFeedMalwareSample**](DatabasesThreatFeedApi.md#downloadThreatFeedMalwareSample) | **GET** /v3.4/download/threat-feed/malware/sample | Download a sample of the malware threat feed (CSV) |
| [**downloadThreatFeedPhishing**](DatabasesThreatFeedApi.md#downloadThreatFeedPhishing) | **GET** /v3.4/download/threat-feed/phishing | Download the daily phishing threat feed (CSV) |
| [**downloadThreatFeedPhishingSample**](DatabasesThreatFeedApi.md#downloadThreatFeedPhishingSample) | **GET** /v3.4/download/threat-feed/phishing/sample | Download a sample of the phishing threat feed (CSV) |
| [**downloadThreatFeedSpam**](DatabasesThreatFeedApi.md#downloadThreatFeedSpam) | **GET** /v3.4/download/threat-feed/spam | Download the daily spam threat feed (CSV) |
| [**downloadThreatFeedSpamSample**](DatabasesThreatFeedApi.md#downloadThreatFeedSpamSample) | **GET** /v3.4/download/threat-feed/spam/sample | Download a sample of the spam threat feed (CSV) |


<a id="downloadThreatFeedMalware"></a>
# **downloadThreatFeedMalware**
> File downloadThreatFeedMalware(date)

Download the daily malware threat feed (CSV)

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.DatabasesThreatFeedApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DatabasesThreatFeedApi apiInstance = new DatabasesThreatFeedApi(defaultClient);
    String date = "date_example"; // String | Feed date (yyyy-MM-dd); defaults to latest available
    try {
      File result = apiInstance.downloadThreatFeedMalware(date);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatabasesThreatFeedApi#downloadThreatFeedMalware");
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
| **date** | **String**| Feed date (yyyy-MM-dd); defaults to latest available | [optional] |

### Return type

[**File**](File.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/octet-stream

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Malware threat feed as CSV (domain,threat_type,confidence,first_seen,last_seen,No_of_threat_matched_pivots) |  -  |

<a id="downloadThreatFeedMalwareSample"></a>
# **downloadThreatFeedMalwareSample**
> File downloadThreatFeedMalwareSample()

Download a sample of the malware threat feed (CSV)

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.DatabasesThreatFeedApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DatabasesThreatFeedApi apiInstance = new DatabasesThreatFeedApi(defaultClient);
    try {
      File result = apiInstance.downloadThreatFeedMalwareSample();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatabasesThreatFeedApi#downloadThreatFeedMalwareSample");
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

[**File**](File.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/octet-stream

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Sample malware threat feed as CSV |  -  |

<a id="downloadThreatFeedPhishing"></a>
# **downloadThreatFeedPhishing**
> File downloadThreatFeedPhishing(date)

Download the daily phishing threat feed (CSV)

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.DatabasesThreatFeedApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DatabasesThreatFeedApi apiInstance = new DatabasesThreatFeedApi(defaultClient);
    String date = "date_example"; // String | Feed date (yyyy-MM-dd); defaults to latest available
    try {
      File result = apiInstance.downloadThreatFeedPhishing(date);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatabasesThreatFeedApi#downloadThreatFeedPhishing");
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
| **date** | **String**| Feed date (yyyy-MM-dd); defaults to latest available | [optional] |

### Return type

[**File**](File.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/octet-stream

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Phishing threat feed as CSV (domain,threat_type,confidence,first_seen,last_seen,No_of_threat_matched_pivots) |  -  |

<a id="downloadThreatFeedPhishingSample"></a>
# **downloadThreatFeedPhishingSample**
> File downloadThreatFeedPhishingSample()

Download a sample of the phishing threat feed (CSV)

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.DatabasesThreatFeedApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DatabasesThreatFeedApi apiInstance = new DatabasesThreatFeedApi(defaultClient);
    try {
      File result = apiInstance.downloadThreatFeedPhishingSample();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatabasesThreatFeedApi#downloadThreatFeedPhishingSample");
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

[**File**](File.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/octet-stream

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Sample phishing threat feed as CSV |  -  |

<a id="downloadThreatFeedSpam"></a>
# **downloadThreatFeedSpam**
> File downloadThreatFeedSpam(date)

Download the daily spam threat feed (CSV)

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.DatabasesThreatFeedApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DatabasesThreatFeedApi apiInstance = new DatabasesThreatFeedApi(defaultClient);
    String date = "date_example"; // String | Feed date (yyyy-MM-dd); defaults to latest available
    try {
      File result = apiInstance.downloadThreatFeedSpam(date);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatabasesThreatFeedApi#downloadThreatFeedSpam");
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
| **date** | **String**| Feed date (yyyy-MM-dd); defaults to latest available | [optional] |

### Return type

[**File**](File.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/octet-stream

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Spam threat feed as CSV (domain,threat_type,confidence,first_seen,last_seen,No_of_threat_matched_pivots) |  -  |

<a id="downloadThreatFeedSpamSample"></a>
# **downloadThreatFeedSpamSample**
> File downloadThreatFeedSpamSample()

Download a sample of the spam threat feed (CSV)

### Example
```java
// Import classes:
import com.whoisfreaks.client.ApiClient;
import com.whoisfreaks.client.ApiException;
import com.whoisfreaks.client.Configuration;
import com.whoisfreaks.client.auth.*;
import com.whoisfreaks.client.models.*;
import com.whoisfreaks.client.api.DatabasesThreatFeedApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DatabasesThreatFeedApi apiInstance = new DatabasesThreatFeedApi(defaultClient);
    try {
      File result = apiInstance.downloadThreatFeedSpamSample();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatabasesThreatFeedApi#downloadThreatFeedSpamSample");
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

[**File**](File.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/octet-stream

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Sample spam threat feed as CSV |  -  |

