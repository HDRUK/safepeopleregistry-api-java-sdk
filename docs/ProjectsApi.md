# ProjectsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**projectsDelete**](ProjectsApi.md#projectsDelete) | **DELETE** /api/v1/project_users/{id} | ProjectHasUser@delete |
| [**projectsGetValidatedProjects**](ProjectsApi.md#projectsGetValidatedProjects) | **GET** /api/v1/projects/user/{registryId}/validated | Project@getValidatedProjects |


<a id="projectsDelete"></a>
# **projectsDelete**
> projectsDelete(id)

ProjectHasUser@delete

Delete a user from a project

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ProjectsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ProjectsApi apiInstance = new ProjectsApi(defaultClient);
    Integer id = 1; // Integer | ID
    try {
      apiInstance.projectsDelete(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProjectsApi#projectsDelete");
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
| **id** | **Integer**| ID | |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | success |  -  |
| **400** | Invalid argument(s) |  -  |
| **404** | failed |  -  |

<a id="projectsGetValidatedProjects"></a>
# **projectsGetValidatedProjects**
> OrganisationGetProjects200Response projectsGetValidatedProjects(registryId)

Project@getValidatedProjects

Return (approved) projects for a registry (user)

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ProjectsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ProjectsApi apiInstance = new ProjectsApi(defaultClient);
    Integer registryId = 1; // Integer | Registry ID
    try {
      OrganisationGetProjects200Response result = apiInstance.projectsGetValidatedProjects(registryId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProjectsApi#projectsGetValidatedProjects");
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
| **registryId** | **Integer**| Registry ID | |

### Return type

[**OrganisationGetProjects200Response**](OrganisationGetProjects200Response.md)

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

