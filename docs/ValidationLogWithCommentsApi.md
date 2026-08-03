# ValidationLogWithCommentsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**validationLogWithCommentsIndex**](ValidationLogWithCommentsApi.md#validationLogWithCommentsIndex) | **GET** /api/v1/validation_logs/{id} | Get  a Validation Log |


<a id="validationLogWithCommentsIndex"></a>
# **validationLogWithCommentsIndex**
> List&lt;ValidationLog&gt; validationLogWithCommentsIndex(id)

Get  a Validation Log

Retrieve a specific entry for a validation log .

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ValidationLogWithCommentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ValidationLogWithCommentsApi apiInstance = new ValidationLogWithCommentsApi(defaultClient);
    Integer id = 56; // Integer | The ID of the validation log
    try {
      List<ValidationLog> result = apiInstance.validationLogWithCommentsIndex(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ValidationLogWithCommentsApi#validationLogWithCommentsIndex");
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
| **id** | **Integer**| The ID of the validation log | |

### Return type

[**List&lt;ValidationLog&gt;**](ValidationLog.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Validation log with comments |  -  |
| **404** | Validation log not found |  -  |

