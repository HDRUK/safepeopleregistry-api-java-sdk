# ProjectHasOrganisationApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**projectHasOrganisationShow**](ProjectHasOrganisationApi.md#projectHasOrganisationShow) | **GET** /api/v1/project-organisations/{projectOrganisationId} | Get details of a project-organisation relationship |


<a id="projectHasOrganisationShow"></a>
# **projectHasOrganisationShow**
> ProjectHasOrganisation projectHasOrganisationShow(projectOrganisationId)

Get details of a project-organisation relationship

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ProjectHasOrganisationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ProjectHasOrganisationApi apiInstance = new ProjectHasOrganisationApi(defaultClient);
    Integer projectOrganisationId = 1; // Integer | ID of the project-organisation relationship
    try {
      ProjectHasOrganisation result = apiInstance.projectHasOrganisationShow(projectOrganisationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProjectHasOrganisationApi#projectHasOrganisationShow");
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
| **projectOrganisationId** | **Integer**| ID of the project-organisation relationship | |

### Return type

[**ProjectHasOrganisation**](ProjectHasOrganisation.md)

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
| **404** | Project-organisation relationship not found |  -  |
| **500** | Internal server error |  -  |

