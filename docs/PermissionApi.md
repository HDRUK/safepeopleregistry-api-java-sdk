# PermissionApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**permissionDestroy**](PermissionApi.md#permissionDestroy) | **DELETE** /api/v1/permissions/{id} | Permission@destroy |
| [**permissionIndex**](PermissionApi.md#permissionIndex) | **GET** /api/v1/permissions | Permission@index |
| [**permissionShow**](PermissionApi.md#permissionShow) | **GET** /api/v1/permissions/{id} | Permission@show |
| [**permissionStore**](PermissionApi.md#permissionStore) | **POST** /api/v1/permissions | Permission@store |
| [**permissionUpdate**](PermissionApi.md#permissionUpdate) | **PATCH** /api/v1/permissions/{id} | Permission@update |


<a id="permissionDestroy"></a>
# **permissionDestroy**
> AffiliationDestroy200Response permissionDestroy(id)

Permission@destroy

Delete a Permission entry from the system

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.PermissionApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    PermissionApi apiInstance = new PermissionApi(defaultClient);
    Integer id = 1; // Integer | Permission entry ID
    try {
      AffiliationDestroy200Response result = apiInstance.permissionDestroy(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PermissionApi#permissionDestroy");
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
| **id** | **Integer**| Permission entry ID | |

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
| **404** | Not found response |  -  |
| **200** | Success |  -  |
| **500** | Error |  -  |

<a id="permissionIndex"></a>
# **permissionIndex**
> PermissionIndex200Response permissionIndex()

Permission@index

Return a list of Permissions

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.PermissionApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    PermissionApi apiInstance = new PermissionApi(defaultClient);
    try {
      PermissionIndex200Response result = apiInstance.permissionIndex();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PermissionApi#permissionIndex");
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

[**PermissionIndex200Response**](PermissionIndex200Response.md)

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

<a id="permissionShow"></a>
# **permissionShow**
> PermissionIndex200Response permissionShow(id)

Permission@show

Return a Permission entry by ID

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.PermissionApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    PermissionApi apiInstance = new PermissionApi(defaultClient);
    Integer id = 1; // Integer | Permission entry ID
    try {
      PermissionIndex200Response result = apiInstance.permissionShow(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PermissionApi#permissionShow");
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
| **id** | **Integer**| Permission entry ID | |

### Return type

[**PermissionIndex200Response**](PermissionIndex200Response.md)

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

<a id="permissionStore"></a>
# **permissionStore**
> AccreditationStoreByRegistryId201Response permissionStore(permissionStoreRequest)

Permission@store

Create a Permission entry

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.PermissionApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    PermissionApi apiInstance = new PermissionApi(defaultClient);
    PermissionStoreRequest permissionStoreRequest = new PermissionStoreRequest(); // PermissionStoreRequest | Permission definition
    try {
      AccreditationStoreByRegistryId201Response result = apiInstance.permissionStore(permissionStoreRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PermissionApi#permissionStore");
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
| **permissionStoreRequest** | [**PermissionStoreRequest**](PermissionStoreRequest.md)| Permission definition | |

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

<a id="permissionUpdate"></a>
# **permissionUpdate**
> PermissionUpdate200Response permissionUpdate(id, permissionStoreRequest)

Permission@update

Update a Permission entry

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.PermissionApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    PermissionApi apiInstance = new PermissionApi(defaultClient);
    Integer id = 1; // Integer | Permission entry ID
    PermissionStoreRequest permissionStoreRequest = new PermissionStoreRequest(); // PermissionStoreRequest | Permission definition
    try {
      PermissionUpdate200Response result = apiInstance.permissionUpdate(id, permissionStoreRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PermissionApi#permissionUpdate");
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
| **id** | **Integer**| Permission entry ID | |
| **permissionStoreRequest** | [**PermissionStoreRequest**](PermissionStoreRequest.md)| Permission definition | |

### Return type

[**PermissionUpdate200Response**](PermissionUpdate200Response.md)

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
| **500** | Error |  -  |

