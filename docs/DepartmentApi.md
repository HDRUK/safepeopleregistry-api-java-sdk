# DepartmentApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**departmentDestroy**](DepartmentApi.md#departmentDestroy) | **DELETE** /api/v1/departments/{id} | Delete a department |
| [**departmentIndex**](DepartmentApi.md#departmentIndex) | **GET** /api/v1/departments | Get a list of departments |
| [**departmentShow**](DepartmentApi.md#departmentShow) | **GET** /api/v1/departments/{id} | Get a specific department by ID |
| [**departmentStore**](DepartmentApi.md#departmentStore) | **POST** /api/v1/departments | Create a new department |
| [**departmentUpdate**](DepartmentApi.md#departmentUpdate) | **PUT** /api/v1/departments/{id} | Update an existing department |


<a id="departmentDestroy"></a>
# **departmentDestroy**
> AffiliationDestroy200Response departmentDestroy(id)

Delete a department

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.DepartmentApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    DepartmentApi apiInstance = new DepartmentApi(defaultClient);
    Integer id = 1; // Integer | ID of the department
    try {
      AffiliationDestroy200Response result = apiInstance.departmentDestroy(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DepartmentApi#departmentDestroy");
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
| **id** | **Integer**| ID of the department | |

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
| **200** | Deleted |  -  |
| **400** | Invalid argument(s) |  -  |
| **404** | Department not found |  -  |

<a id="departmentIndex"></a>
# **departmentIndex**
> List&lt;Department&gt; departmentIndex()

Get a list of departments

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.DepartmentApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    DepartmentApi apiInstance = new DepartmentApi(defaultClient);
    try {
      List<Department> result = apiInstance.departmentIndex();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DepartmentApi#departmentIndex");
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

[**List&lt;Department&gt;**](Department.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

<a id="departmentShow"></a>
# **departmentShow**
> Department departmentShow(id)

Get a specific department by ID

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.DepartmentApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    DepartmentApi apiInstance = new DepartmentApi(defaultClient);
    Integer id = 1; // Integer | ID of the department
    try {
      Department result = apiInstance.departmentShow(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DepartmentApi#departmentShow");
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
| **id** | **Integer**| ID of the department | |

### Return type

[**Department**](Department.md)

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
| **404** | Department not found |  -  |

<a id="departmentStore"></a>
# **departmentStore**
> AccreditationStoreByRegistryId201Response departmentStore(department)

Create a new department

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.DepartmentApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    DepartmentApi apiInstance = new DepartmentApi(defaultClient);
    Department department = new Department(); // Department | 
    try {
      AccreditationStoreByRegistryId201Response result = apiInstance.departmentStore(department);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DepartmentApi#departmentStore");
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
| **department** | [**Department**](Department.md)|  | |

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
| **201** | Created |  -  |
| **400** | Validation error |  -  |

<a id="departmentUpdate"></a>
# **departmentUpdate**
> Department departmentUpdate(id, department)

Update an existing department

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.DepartmentApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    DepartmentApi apiInstance = new DepartmentApi(defaultClient);
    Integer id = 1; // Integer | ID of the department
    Department department = new Department(); // Department | 
    try {
      Department result = apiInstance.departmentUpdate(id, department);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DepartmentApi#departmentUpdate");
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
| **id** | **Integer**| ID of the department | |
| **department** | [**Department**](Department.md)|  | |

### Return type

[**Department**](Department.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Updated |  -  |
| **400** | Invalid argument(s) |  -  |
| **404** | Department not found |  -  |

