# CustodianApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**custodianAddProject**](CustodianApi.md#custodianAddProject) | **POST** /api/v1/custodians/{custodianId}/projects | Custodian@addProject |
| [**custodianDestroy**](CustodianApi.md#custodianDestroy) | **DELETE** /api/v1/custodians/{id} | Custodian@destroy |
| [**custodianGetOrganisations**](CustodianApi.md#custodianGetOrganisations) | **GET** /api/v1/custodian/{custodianId}/organisations | Return all custodian organisations with projects |
| [**custodianGetProjects**](CustodianApi.md#custodianGetProjects) | **GET** /api/v1/custodian/{custodianId}/projects | Return all projects associated with a custodian |
| [**custodianGetProjectsUsers**](CustodianApi.md#custodianGetProjectsUsers) | **GET** /api/v1/custodians/{custodianId}/projects_users | Get all users associated with custodian&#39;s projects |
| [**custodianGetUserProjects**](CustodianApi.md#custodianGetUserProjects) | **GET** /api/v1/custodian/{custodianId}/users/{userId}/projects | Return all custodian projects associated with a user |
| [**custodianIndex**](CustodianApi.md#custodianIndex) | **GET** /api/v1/custodians | Custodian@index |
| [**custodianShow**](CustodianApi.md#custodianShow) | **GET** /api/v1/custodians/{id} | Custodian@show |
| [**custodianShowByUniqueIdentifier**](CustodianApi.md#custodianShowByUniqueIdentifier) | **GET** /api/v1/custodians/identifier/{id} | Custodian@showByUniqueIdentifier |
| [**custodianStore**](CustodianApi.md#custodianStore) | **POST** /api/v1/custodians | Custodian@store |
| [**custodianUpdate**](CustodianApi.md#custodianUpdate) | **PUT** /api/v1/custodians/{id} | Custodian@update |


<a id="custodianAddProject"></a>
# **custodianAddProject**
> CustodianAddProject201Response custodianAddProject(custodianId, custodianAddProjectRequest)

Custodian@addProject

Create a project for a custodian

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.CustodianApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CustodianApi apiInstance = new CustodianApi(defaultClient);
    Integer custodianId = 56; // Integer | ID of the custodian
    CustodianAddProjectRequest custodianAddProjectRequest = new CustodianAddProjectRequest(); // CustodianAddProjectRequest | Project definition
    try {
      CustodianAddProject201Response result = apiInstance.custodianAddProject(custodianId, custodianAddProjectRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustodianApi#custodianAddProject");
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
| **custodianId** | **Integer**| ID of the custodian | |
| **custodianAddProjectRequest** | [**CustodianAddProjectRequest**](CustodianAddProjectRequest.md)| Project definition | |

### Return type

[**CustodianAddProject201Response**](CustodianAddProject201Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Success |  -  |
| **400** | Invalid argument(s) |  -  |
| **500** | Error |  -  |

<a id="custodianDestroy"></a>
# **custodianDestroy**
> AffiliationDestroy200Response custodianDestroy(id)

Custodian@destroy

Delete a Custodian entry from the system

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.CustodianApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CustodianApi apiInstance = new CustodianApi(defaultClient);
    Integer id = 1; // Integer | Custodian entry ID
    try {
      AffiliationDestroy200Response result = apiInstance.custodianDestroy(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustodianApi#custodianDestroy");
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
| **id** | **Integer**| Custodian entry ID | |

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
| **400** | Invalid argument(s) |  -  |
| **404** | Not found response |  -  |
| **200** | Success |  -  |
| **500** | Error |  -  |

<a id="custodianGetOrganisations"></a>
# **custodianGetOrganisations**
> CustodianGetOrganisations200Response custodianGetOrganisations(custodianId)

Return all custodian organisations with projects

Fetch a list of custodians organisations with projects, along with pagination details.

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.CustodianApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CustodianApi apiInstance = new CustodianApi(defaultClient);
    Integer custodianId = 1; // Integer | The ID of the custodian whose organisations are to be retrieved
    try {
      CustodianGetOrganisations200Response result = apiInstance.custodianGetOrganisations(custodianId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustodianApi#custodianGetOrganisations");
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
| **custodianId** | **Integer**| The ID of the custodian whose organisations are to be retrieved | |

### Return type

[**CustodianGetOrganisations200Response**](CustodianGetOrganisations200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

<a id="custodianGetProjects"></a>
# **custodianGetProjects**
> CustodianGetProjects200Response custodianGetProjects(custodianId)

Return all projects associated with a custodian

Fetch a list of projects along with pagination details for a specified custodian.

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.CustodianApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CustodianApi apiInstance = new CustodianApi(defaultClient);
    Integer custodianId = 1; // Integer | The ID of the custodian whose projects are to be retrieved
    try {
      CustodianGetProjects200Response result = apiInstance.custodianGetProjects(custodianId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustodianApi#custodianGetProjects");
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
| **custodianId** | **Integer**| The ID of the custodian whose projects are to be retrieved | |

### Return type

[**CustodianGetProjects200Response**](CustodianGetProjects200Response.md)

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
| **404** | Custodian not found |  -  |

<a id="custodianGetProjectsUsers"></a>
# **custodianGetProjectsUsers**
> CustodianGetProjectsUsers200Response custodianGetProjectsUsers(custodianId)

Get all users associated with custodian&#39;s projects

Returns paginated users for all projects under a specific custodian.

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.CustodianApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CustodianApi apiInstance = new CustodianApi(defaultClient);
    Integer custodianId = 56; // Integer | Custodian ID
    try {
      CustodianGetProjectsUsers200Response result = apiInstance.custodianGetProjectsUsers(custodianId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustodianApi#custodianGetProjectsUsers");
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
| **custodianId** | **Integer**| Custodian ID | |

### Return type

[**CustodianGetProjectsUsers200Response**](CustodianGetProjectsUsers200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | List of users |  -  |
| **400** | Invalid argument(s) |  -  |
| **404** | Custodian not found |  -  |

<a id="custodianGetUserProjects"></a>
# **custodianGetUserProjects**
> CustodianGetUserProjects200Response custodianGetUserProjects(custodianId, userId)

Return all custodian projects associated with a user

Fetch a list of custodians projects associated with a user, along with pagination details.

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.CustodianApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CustodianApi apiInstance = new CustodianApi(defaultClient);
    Integer custodianId = 1; // Integer | The ID of the custodian whose projects are to be retrieved
    Integer userId = 1; // Integer | The ID of the user whose projects are to be retrieved
    try {
      CustodianGetUserProjects200Response result = apiInstance.custodianGetUserProjects(custodianId, userId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustodianApi#custodianGetUserProjects");
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
| **custodianId** | **Integer**| The ID of the custodian whose projects are to be retrieved | |
| **userId** | **Integer**| The ID of the user whose projects are to be retrieved | |

### Return type

[**CustodianGetUserProjects200Response**](CustodianGetUserProjects200Response.md)

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
| **404** | User not found |  -  |

<a id="custodianIndex"></a>
# **custodianIndex**
> CustodianIndex200Response custodianIndex()

Custodian@index

Return a list of Custodians

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.CustodianApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CustodianApi apiInstance = new CustodianApi(defaultClient);
    try {
      CustodianIndex200Response result = apiInstance.custodianIndex();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustodianApi#custodianIndex");
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

[**CustodianIndex200Response**](CustodianIndex200Response.md)

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

<a id="custodianShow"></a>
# **custodianShow**
> CustodianIndex200Response custodianShow(id)

Custodian@show

Return an Custodian entry by ID

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.CustodianApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CustodianApi apiInstance = new CustodianApi(defaultClient);
    Integer id = 1; // Integer | Custodian ID
    try {
      CustodianIndex200Response result = apiInstance.custodianShow(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustodianApi#custodianShow");
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
| **id** | **Integer**| Custodian ID | |

### Return type

[**CustodianIndex200Response**](CustodianIndex200Response.md)

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

<a id="custodianShowByUniqueIdentifier"></a>
# **custodianShowByUniqueIdentifier**
> CustodianIndex200Response custodianShowByUniqueIdentifier(id)

Custodian@showByUniqueIdentifier

Return an Custodian entry by Unique Identifier

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.CustodianApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CustodianApi apiInstance = new CustodianApi(defaultClient);
    String id = "c3eddb33-db74-4ea7-961a-778740f17e25"; // String | Custodian Unique Identifier
    try {
      CustodianIndex200Response result = apiInstance.custodianShowByUniqueIdentifier(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustodianApi#custodianShowByUniqueIdentifier");
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
| **id** | **String**| Custodian Unique Identifier | |

### Return type

[**CustodianIndex200Response**](CustodianIndex200Response.md)

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

<a id="custodianStore"></a>
# **custodianStore**
> CustodianStore201Response custodianStore(custodianStoreRequest)

Custodian@store

Create a Custodian entry

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.CustodianApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CustodianApi apiInstance = new CustodianApi(defaultClient);
    CustodianStoreRequest custodianStoreRequest = new CustodianStoreRequest(); // CustodianStoreRequest | Custodian definition
    try {
      CustodianStore201Response result = apiInstance.custodianStore(custodianStoreRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustodianApi#custodianStore");
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
| **custodianStoreRequest** | [**CustodianStoreRequest**](CustodianStoreRequest.md)| Custodian definition | |

### Return type

[**CustodianStore201Response**](CustodianStore201Response.md)

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

<a id="custodianUpdate"></a>
# **custodianUpdate**
> CustodianStore201Response custodianUpdate(id, custodianStoreRequest)

Custodian@update

Edit a Custodian entry

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.CustodianApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CustodianApi apiInstance = new CustodianApi(defaultClient);
    Integer id = 1; // Integer | Custodian ID
    CustodianStoreRequest custodianStoreRequest = new CustodianStoreRequest(); // CustodianStoreRequest | Custodian definition
    try {
      CustodianStore201Response result = apiInstance.custodianUpdate(id, custodianStoreRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustodianApi#custodianUpdate");
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
| **id** | **Integer**| Custodian ID | |
| **custodianStoreRequest** | [**CustodianStoreRequest**](CustodianStoreRequest.md)| Custodian definition | |

### Return type

[**CustodianStore201Response**](CustodianStore201Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **400** | Invalid argument(s) |  -  |
| **404** | Not found response |  -  |
| **200** | Success |  -  |
| **500** | Error |  -  |

