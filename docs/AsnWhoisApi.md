# AsnWhoisApi

All URIs are relative to *https://api.whoisfreaks.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**asnWhois**](AsnWhoisApi.md#asnWhois) | **GET** /v2.0/asn-whois | ASN WHOIS Lookup |


<a id="asnWhois"></a>
# **asnWhois**
> AsnWhoisResponse asnWhois(asn, format)

ASN WHOIS Lookup

WHOIS for an ASN. 1 credit.

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
import com.whoisfreaks.client.api.AsnWhoisApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.whoisfreaks.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AsnWhoisApi apiInstance = new AsnWhoisApi(defaultClient);
    String asn = "as15169"; // String | 
    String format = "json"; // String | 
    try {
      AsnWhoisResponse result = apiInstance.asnWhois(asn, format);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AsnWhoisApi#asnWhois");
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
| **asn** | **String**|  | |
| **format** | **String**|  | [optional] [default to json] [enum: json, xml] |

### Return type

[**AsnWhoisResponse**](AsnWhoisResponse.md)

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

