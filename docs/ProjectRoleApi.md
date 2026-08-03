# ProjectRoleApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**projectRoleIndex**](ProjectRoleApi.md#projectRoleIndex) | **GET** /api/v1/project_roles | ProjectRole@index |
| [**projectRoleShow**](ProjectRoleApi.md#projectRoleShow) | **GET** /api/v1/project_roles/{id} | ProjectRole@show |
| [**projectRoleStore**](ProjectRoleApi.md#projectRoleStore) | **POST** /api/v1/project_roles | ProjectRole@store |
| [**projectRoleUpdate**](ProjectRoleApi.md#projectRoleUpdate) | **PUT** /api/v1/project_roles/{id} | ProjectRole@update |


<a id="projectRoleIndex"></a>
# **projectRoleIndex**
> ProjectRoleIndex200Response projectRoleIndex()

ProjectRole@index

Return a list of ProjectRole

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ProjectRoleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ProjectRoleApi apiInstance = new ProjectRoleApi(defaultClient);
    try {
      ProjectRoleIndex200Response result = apiInstance.projectRoleIndex();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProjectRoleApi#projectRoleIndex");
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

[**ProjectRoleIndex200Response**](ProjectRoleIndex200Response.md)

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

<a id="projectRoleShow"></a>
# **projectRoleShow**
> ProjectRoleIndex200Response projectRoleShow(id)

ProjectRole@show

Return a ProjectRole

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ProjectRoleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ProjectRoleApi apiInstance = new ProjectRoleApi(defaultClient);
    Integer id = 1; // Integer | ProjectRole entry ID
    try {
      ProjectRoleIndex200Response result = apiInstance.projectRoleShow(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProjectRoleApi#projectRoleShow");
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
| **id** | **Integer**| ProjectRole entry ID | |

### Return type

[**ProjectRoleIndex200Response**](ProjectRoleIndex200Response.md)

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

<a id="projectRoleStore"></a>
# **projectRoleStore**
> IdentityStore201Response projectRoleStore(projectRole)

ProjectRole@store

Create a ProjectRole

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ProjectRoleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ProjectRoleApi apiInstance = new ProjectRoleApi(defaultClient);
    ProjectRole projectRole = new ProjectRole(); // ProjectRole | ProjectRole definition
    try {
      IdentityStore201Response result = apiInstance.projectRoleStore(projectRole);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProjectRoleApi#projectRoleStore");
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
| **projectRole** | [**ProjectRole**](ProjectRole.md)| ProjectRole definition | |

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
| **201** | Success |  -  |
| **404** | Not found response |  -  |
| **500** | Error |  -  |

<a id="projectRoleUpdate"></a>
# **projectRoleUpdate**
> ProjectRoleUpdate200Response projectRoleUpdate(id, projectRole)

ProjectRole@update

Update a ProjectRole entry

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ProjectRoleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ProjectRoleApi apiInstance = new ProjectRoleApi(defaultClient);
    Integer id = 1; // Integer | ProjectRole entry ID
    ProjectRole projectRole = new ProjectRole(); // ProjectRole | ProjectRole definition
    try {
      ProjectRoleUpdate200Response result = apiInstance.projectRoleUpdate(id, projectRole);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProjectRoleApi#projectRoleUpdate");
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
| **id** | **Integer**| ProjectRole entry ID | |
| **projectRole** | [**ProjectRole**](ProjectRole.md)| ProjectRole definition | |

### Return type

[**ProjectRoleUpdate200Response**](ProjectRoleUpdate200Response.md)

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

