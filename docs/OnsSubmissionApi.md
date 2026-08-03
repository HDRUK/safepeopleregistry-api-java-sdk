# OnsSubmissionApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**oNSSubmissionReceiveCSV**](OnsSubmissionApi.md#oNSSubmissionReceiveCSV) | **POST** /api/v1/ons-submissions/csv | Upload a CSV file for ONS submission |


<a id="oNSSubmissionReceiveCSV"></a>
# **oNSSubmissionReceiveCSV**
> ONSSubmissionReceiveCSV200Response oNSSubmissionReceiveCSV(_file)

Upload a CSV file for ONS submission

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.OnsSubmissionApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    OnsSubmissionApi apiInstance = new OnsSubmissionApi(defaultClient);
    File _file = new File("/path/to/file"); // File | CSV file to upload
    try {
      ONSSubmissionReceiveCSV200Response result = apiInstance.oNSSubmissionReceiveCSV(_file);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OnsSubmissionApi#oNSSubmissionReceiveCSV");
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
| **_file** | **File**| CSV file to upload | [optional] |

### Return type

[**ONSSubmissionReceiveCSV200Response**](ONSSubmissionReceiveCSV200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | File uploaded successfully |  -  |
| **400** | File upload failed |  -  |

