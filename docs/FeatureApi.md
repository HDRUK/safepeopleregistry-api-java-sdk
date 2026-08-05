# FeatureApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**featureIndex**](FeatureApi.md#featureIndex) | **GET** /api/v1/features | Feature@index |


<a id="featureIndex"></a>
# **featureIndex**
> FeatureIndex200Response featureIndex()

Feature@index

Return a list of Feature entries

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.FeatureApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    FeatureApi apiInstance = new FeatureApi(defaultClient);
    try {
      FeatureIndex200Response result = apiInstance.featureIndex();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FeatureApi#featureIndex");
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

[**FeatureIndex200Response**](FeatureIndex200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **404** | Not found response |  -  |

