# AffiliationApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**affiliationDestroy**](AffiliationApi.md#affiliationDestroy) | **DELETE** /api/v1/training/{id} | Affiliation@destroy |


<a id="affiliationDestroy"></a>
# **affiliationDestroy**
> AffiliationDestroy200Response affiliationDestroy(id)

Affiliation@destroy

Delete a affiliation entry from the system

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.AffiliationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    AffiliationApi apiInstance = new AffiliationApi(defaultClient);
    Integer id = 1; // Integer | Affiliation entry ID
    try {
      AffiliationDestroy200Response result = apiInstance.affiliationDestroy(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AffiliationApi#affiliationDestroy");
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
| **id** | **Integer**| Affiliation entry ID | |

### Return type

[**AffiliationDestroy200Response**](AffiliationDestroy200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **400** | Invalid argument(s) |  -  |
| **404** | Not found response |  -  |
| **500** | Error |  -  |

