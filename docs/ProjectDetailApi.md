# ProjectDetailApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**projectDetailIndex**](ProjectDetailApi.md#projectDetailIndex) | **GET** /api/v1/project_details | ProjectDetail@index |
| [**projectDetailShow**](ProjectDetailApi.md#projectDetailShow) | **GET** /api/v1/project_details/{id} | ProjectDetail@show |


<a id="projectDetailIndex"></a>
# **projectDetailIndex**
> ProjectDetailIndex200Response projectDetailIndex()

ProjectDetail@index

Return a list of ProjectDetail

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ProjectDetailApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ProjectDetailApi apiInstance = new ProjectDetailApi(defaultClient);
    try {
      ProjectDetailIndex200Response result = apiInstance.projectDetailIndex();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProjectDetailApi#projectDetailIndex");
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

[**ProjectDetailIndex200Response**](ProjectDetailIndex200Response.md)

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

<a id="projectDetailShow"></a>
# **projectDetailShow**
> ProjectDetailIndex200Response projectDetailShow(id)

ProjectDetail@show

Return a ProjectDetail

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ProjectDetailApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ProjectDetailApi apiInstance = new ProjectDetailApi(defaultClient);
    Integer id = 1; // Integer | ProjectDetail entry ID
    try {
      ProjectDetailIndex200Response result = apiInstance.projectDetailShow(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProjectDetailApi#projectDetailShow");
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
| **id** | **Integer**| ProjectDetail entry ID | |

### Return type

[**ProjectDetailIndex200Response**](ProjectDetailIndex200Response.md)

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

