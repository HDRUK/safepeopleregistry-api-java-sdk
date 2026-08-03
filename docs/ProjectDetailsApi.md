# ProjectDetailsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**projectDetailsDestroy**](ProjectDetailsApi.md#projectDetailsDestroy) | **DELETE** /api/v1/project_details/{id} | ProjectDetails@destroy |
| [**projectDetailsStore**](ProjectDetailsApi.md#projectDetailsStore) | **POST** /api/v1/project_details | ProjectDetails@store |
| [**projectDetailsUpdate**](ProjectDetailsApi.md#projectDetailsUpdate) | **PUT** /api/v1/project_details/{id} | ProjectDetails@update |


<a id="projectDetailsDestroy"></a>
# **projectDetailsDestroy**
> AffiliationDestroy200Response projectDetailsDestroy(id)

ProjectDetails@destroy

Delete a ProjectDetail entry from the system

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ProjectDetailsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ProjectDetailsApi apiInstance = new ProjectDetailsApi(defaultClient);
    Integer id = 1; // Integer | ProjectDetails entry ID
    try {
      AffiliationDestroy200Response result = apiInstance.projectDetailsDestroy(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProjectDetailsApi#projectDetailsDestroy");
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
| **id** | **Integer**| ProjectDetails entry ID | |

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

<a id="projectDetailsStore"></a>
# **projectDetailsStore**
> IdentityStore201Response projectDetailsStore(projectDetail)

ProjectDetails@store

Create a ProjectDetail

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ProjectDetailsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ProjectDetailsApi apiInstance = new ProjectDetailsApi(defaultClient);
    ProjectDetail projectDetail = new ProjectDetail(); // ProjectDetail | ProjectDetail definition
    try {
      IdentityStore201Response result = apiInstance.projectDetailsStore(projectDetail);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProjectDetailsApi#projectDetailsStore");
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
| **projectDetail** | [**ProjectDetail**](ProjectDetail.md)| ProjectDetail definition | |

### Return type

[**IdentityStore201Response**](IdentityStore201Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **404** | Not found response |  -  |
| **201** | Success |  -  |
| **500** | Error |  -  |

<a id="projectDetailsUpdate"></a>
# **projectDetailsUpdate**
> ProjectDetailsUpdate200Response projectDetailsUpdate(id, projectDetail)

ProjectDetails@update

Update a ProjectDetail entry

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ProjectDetailsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ProjectDetailsApi apiInstance = new ProjectDetailsApi(defaultClient);
    Integer id = 1; // Integer | ProjectDetails entry ID
    ProjectDetail projectDetail = new ProjectDetail(); // ProjectDetail | ProjectDetails definition
    try {
      ProjectDetailsUpdate200Response result = apiInstance.projectDetailsUpdate(id, projectDetail);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProjectDetailsApi#projectDetailsUpdate");
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
| **id** | **Integer**| ProjectDetails entry ID | |
| **projectDetail** | [**ProjectDetail**](ProjectDetail.md)| ProjectDetails definition | |

### Return type

[**ProjectDetailsUpdate200Response**](ProjectDetailsUpdate200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **400** | Invalid argument(s) |  -  |
| **404** | Not found response |  -  |
| **500** | Error |  -  |

