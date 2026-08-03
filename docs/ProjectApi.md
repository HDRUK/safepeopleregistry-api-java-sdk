# ProjectApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**projectDestroy**](ProjectApi.md#projectDestroy) | **DELETE** /api/v1/projects/{id} | Project@destroy |
| [**projectGetAllUsersFlagProjectByUserId**](ProjectApi.md#projectGetAllUsersFlagProjectByUserId) | **GET** /api/v1/projects/{projectId}/all_users/{userId} | Get all users by projectID and userID |
| [**projectGetProjectByIdAndOrganisationId**](ProjectApi.md#projectGetProjectByIdAndOrganisationId) | **GET** /api/v1/projects/{projectId}/organisations/{organisationId} | Get project details by projectID and organisationID |
| [**projectGetProjectByIdAndUserId**](ProjectApi.md#projectGetProjectByIdAndUserId) | **GET** /api/v1/projects/{projectId}/users/{userId} | Get project details by projectID and userID |
| [**projectGetProjectUsers**](ProjectApi.md#projectGetProjectUsers) | **GET** /api/v1/projects/{id}/users | Project@getProjectUsers |
| [**projectGetProjectUsersByOrganisationId**](ProjectApi.md#projectGetProjectUsersByOrganisationId) | **GET** /api/v1/projects/{projectId}/organisations/{organisationId}/users | Get all users by projectID and organisationID |
| [**projectIndex**](ProjectApi.md#projectIndex) | **GET** /api/v1/projects | Project@index |
| [**projectMakePrimaryContact**](ProjectApi.md#projectMakePrimaryContact) | **PUT** /api/v1/projects/{id}/users/{registryId}/primary_contact | Project@edit |
| [**projectShow**](ProjectApi.md#projectShow) | **GET** /api/v1/projects/{id} | Project@show |
| [**projectStore**](ProjectApi.md#projectStore) | **POST** /api/v1/projects | Project@store |
| [**projectUpdate**](ProjectApi.md#projectUpdate) | **PUT** /api/v1/projects/{id} | Project@update |
| [**projectUpdateAllProjectUsers**](ProjectApi.md#projectUpdateAllProjectUsers) | **PUT** /api/v1/projects/{id}/all_users | Project@updateAllProjectUsers |


<a id="projectDestroy"></a>
# **projectDestroy**
> AffiliationDestroy200Response projectDestroy(id)

Project@destroy

Delete a Project entry from the system

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ProjectApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ProjectApi apiInstance = new ProjectApi(defaultClient);
    Integer id = 1; // Integer | Project entry ID
    try {
      AffiliationDestroy200Response result = apiInstance.projectDestroy(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProjectApi#projectDestroy");
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
| **id** | **Integer**| Project entry ID | |

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

<a id="projectGetAllUsersFlagProjectByUserId"></a>
# **projectGetAllUsersFlagProjectByUserId**
> ProjectGetAllUsersFlagProjectByUserId200Response projectGetAllUsersFlagProjectByUserId(userId, projectId)

Get all users by projectID and userID

Fetches users for a project.

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ProjectApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ProjectApi apiInstance = new ProjectApi(defaultClient);
    Integer userId = 56; // Integer | ID of the user
    Integer projectId = 56; // Integer | ID of the project
    try {
      ProjectGetAllUsersFlagProjectByUserId200Response result = apiInstance.projectGetAllUsersFlagProjectByUserId(userId, projectId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProjectApi#projectGetAllUsersFlagProjectByUserId");
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
| **userId** | **Integer**| ID of the user | |
| **projectId** | **Integer**| ID of the project | |

### Return type

[**ProjectGetAllUsersFlagProjectByUserId200Response**](ProjectGetAllUsersFlagProjectByUserId200Response.md)

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
| **403** | Forbidden |  -  |

<a id="projectGetProjectByIdAndOrganisationId"></a>
# **projectGetProjectByIdAndOrganisationId**
> CustodiansGetOrganisationUsers200Response projectGetProjectByIdAndOrganisationId(organisationId, projectId)

Get project details by projectID and organisationID

Fetches project given organisation and project IDs.

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ProjectApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ProjectApi apiInstance = new ProjectApi(defaultClient);
    Integer organisationId = 56; // Integer | ID of the organisation
    Integer projectId = 56; // Integer | ID of the project
    try {
      CustodiansGetOrganisationUsers200Response result = apiInstance.projectGetProjectByIdAndOrganisationId(organisationId, projectId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProjectApi#projectGetProjectByIdAndOrganisationId");
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
| **organisationId** | **Integer**| ID of the organisation | |
| **projectId** | **Integer**| ID of the project | |

### Return type

[**CustodiansGetOrganisationUsers200Response**](CustodiansGetOrganisationUsers200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved project |  -  |
| **400** | Invalid argument(s) |  -  |
| **404** | Project not found |  -  |

<a id="projectGetProjectByIdAndUserId"></a>
# **projectGetProjectByIdAndUserId**
> ProjectGetProjectByIdAndUserId200Response projectGetProjectByIdAndUserId(userId, projectId)

Get project details by projectID and userID

Fetches project given user and project IDs.

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ProjectApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ProjectApi apiInstance = new ProjectApi(defaultClient);
    Integer userId = 56; // Integer | ID of the user
    Integer projectId = 56; // Integer | ID of the project
    try {
      ProjectGetProjectByIdAndUserId200Response result = apiInstance.projectGetProjectByIdAndUserId(userId, projectId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProjectApi#projectGetProjectByIdAndUserId");
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
| **userId** | **Integer**| ID of the user | |
| **projectId** | **Integer**| ID of the project | |

### Return type

[**ProjectGetProjectByIdAndUserId200Response**](ProjectGetProjectByIdAndUserId200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved project |  -  |
| **400** | Invalid argument(s) |  -  |
| **404** | Project not found |  -  |

<a id="projectGetProjectUsers"></a>
# **projectGetProjectUsers**
> ProjectGetProjectUsers200Response projectGetProjectUsers(id)

Project@getProjectUsers

Return project users by project ID

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ProjectApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ProjectApi apiInstance = new ProjectApi(defaultClient);
    Integer id = 1; // Integer | Project entry ID
    try {
      ProjectGetProjectUsers200Response result = apiInstance.projectGetProjectUsers(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProjectApi#projectGetProjectUsers");
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
| **id** | **Integer**| Project entry ID | |

### Return type

[**ProjectGetProjectUsers200Response**](ProjectGetProjectUsers200Response.md)

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

<a id="projectGetProjectUsersByOrganisationId"></a>
# **projectGetProjectUsersByOrganisationId**
> CustodiansGetOrganisationUsers200Response projectGetProjectUsersByOrganisationId(organisationId, projectId)

Get all users by projectID and organisationID

Fetches users given organisation and project IDs.

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ProjectApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ProjectApi apiInstance = new ProjectApi(defaultClient);
    Integer organisationId = 56; // Integer | ID of the organisation
    Integer projectId = 56; // Integer | ID of the project
    try {
      CustodiansGetOrganisationUsers200Response result = apiInstance.projectGetProjectUsersByOrganisationId(organisationId, projectId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProjectApi#projectGetProjectUsersByOrganisationId");
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
| **organisationId** | **Integer**| ID of the organisation | |
| **projectId** | **Integer**| ID of the project | |

### Return type

[**CustodiansGetOrganisationUsers200Response**](CustodiansGetOrganisationUsers200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved organisation users |  -  |
| **400** | Invalid argument(s) |  -  |
| **404** | Organisation users not found |  -  |

<a id="projectIndex"></a>
# **projectIndex**
> ProjectIndex200Response projectIndex()

Project@index

Return a list of Projects

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ProjectApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ProjectApi apiInstance = new ProjectApi(defaultClient);
    try {
      ProjectIndex200Response result = apiInstance.projectIndex();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProjectApi#projectIndex");
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

[**ProjectIndex200Response**](ProjectIndex200Response.md)

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

<a id="projectMakePrimaryContact"></a>
# **projectMakePrimaryContact**
> ProjectMakePrimaryContact200Response projectMakePrimaryContact(id, registryId, projectMakePrimaryContactRequest)

Project@edit

Make user a primary contact

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ProjectApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ProjectApi apiInstance = new ProjectApi(defaultClient);
    Integer id = 1; // Integer | Project entry ID
    Integer registryId = 1; // Integer | Registry ID
    ProjectMakePrimaryContactRequest projectMakePrimaryContactRequest = new ProjectMakePrimaryContactRequest(); // ProjectMakePrimaryContactRequest | Project definition
    try {
      ProjectMakePrimaryContact200Response result = apiInstance.projectMakePrimaryContact(id, registryId, projectMakePrimaryContactRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProjectApi#projectMakePrimaryContact");
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
| **id** | **Integer**| Project entry ID | |
| **registryId** | **Integer**| Registry ID | |
| **projectMakePrimaryContactRequest** | [**ProjectMakePrimaryContactRequest**](ProjectMakePrimaryContactRequest.md)| Project definition | |

### Return type

[**ProjectMakePrimaryContact200Response**](ProjectMakePrimaryContact200Response.md)

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

<a id="projectShow"></a>
# **projectShow**
> ProjectIndex200Response projectShow(id)

Project@show

Return a Project entry by ID

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ProjectApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ProjectApi apiInstance = new ProjectApi(defaultClient);
    Integer id = 1; // Integer | Project entry ID
    try {
      ProjectIndex200Response result = apiInstance.projectShow(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProjectApi#projectShow");
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
| **id** | **Integer**| Project entry ID | |

### Return type

[**ProjectIndex200Response**](ProjectIndex200Response.md)

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

<a id="projectStore"></a>
# **projectStore**
> AccreditationStoreByRegistryId201Response projectStore(projectStoreRequest)

Project@store

Create a Project entry

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ProjectApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ProjectApi apiInstance = new ProjectApi(defaultClient);
    ProjectStoreRequest projectStoreRequest = new ProjectStoreRequest(); // ProjectStoreRequest | Project definition
    try {
      AccreditationStoreByRegistryId201Response result = apiInstance.projectStore(projectStoreRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProjectApi#projectStore");
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
| **projectStoreRequest** | [**ProjectStoreRequest**](ProjectStoreRequest.md)| Project definition | |

### Return type

[**AccreditationStoreByRegistryId201Response**](AccreditationStoreByRegistryId201Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **404** | Not found response |  -  |
| **200** | Success |  -  |

<a id="projectUpdate"></a>
# **projectUpdate**
> ProjectUpdate200Response projectUpdate(id, projectIndex200ResponseData)

Project@update

Update a Project entry

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ProjectApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ProjectApi apiInstance = new ProjectApi(defaultClient);
    Integer id = 1; // Integer | Project entry ID
    ProjectIndex200ResponseData projectIndex200ResponseData = new ProjectIndex200ResponseData(); // ProjectIndex200ResponseData | Project definition
    try {
      ProjectUpdate200Response result = apiInstance.projectUpdate(id, projectIndex200ResponseData);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProjectApi#projectUpdate");
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
| **id** | **Integer**| Project entry ID | |
| **projectIndex200ResponseData** | [**ProjectIndex200ResponseData**](ProjectIndex200ResponseData.md)| Project definition | |

### Return type

[**ProjectUpdate200Response**](ProjectUpdate200Response.md)

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

<a id="projectUpdateAllProjectUsers"></a>
# **projectUpdateAllProjectUsers**
> ONSSubmissionReceiveCSV200Response projectUpdateAllProjectUsers(id, projectUpdateAllProjectUsersRequest)

Project@updateAllProjectUsers

Update all users associated with a project

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ProjectApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ProjectApi apiInstance = new ProjectApi(defaultClient);
    Integer id = 1; // Integer | Project entry ID
    ProjectUpdateAllProjectUsersRequest projectUpdateAllProjectUsersRequest = new ProjectUpdateAllProjectUsersRequest(); // ProjectUpdateAllProjectUsersRequest | Project definition
    try {
      ONSSubmissionReceiveCSV200Response result = apiInstance.projectUpdateAllProjectUsers(id, projectUpdateAllProjectUsersRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProjectApi#projectUpdateAllProjectUsers");
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
| **id** | **Integer**| Project entry ID | |
| **projectUpdateAllProjectUsersRequest** | [**ProjectUpdateAllProjectUsersRequest**](ProjectUpdateAllProjectUsersRequest.md)| Project definition | |

### Return type

[**ONSSubmissionReceiveCSV200Response**](ONSSubmissionReceiveCSV200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |
| **400** | Invalid argument(s) |  -  |
| **404** | Not found response |  -  |
| **500** | Error |  -  |

