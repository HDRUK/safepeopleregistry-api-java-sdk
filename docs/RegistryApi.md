# RegistryApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**registryDestroy**](RegistryApi.md#registryDestroy) | **DELETE** /api/v1/registry/{id} | Registry@destroy |
| [**registryIndex**](RegistryApi.md#registryIndex) | **GET** /api/v1/registry | Registry@index |
| [**registryShow**](RegistryApi.md#registryShow) | **GET** /api/v1/registry/{id} | Registry@show |
| [**registryStore**](RegistryApi.md#registryStore) | **POST** /api/v1/registry | Registry@store |
| [**registryUpdate**](RegistryApi.md#registryUpdate) | **PUT** /api/v1/registry/{id} | Registry@update |


<a id="registryDestroy"></a>
# **registryDestroy**
> AffiliationDestroy200Response registryDestroy(id)

Registry@destroy

Delete a Registry entry from the system

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.RegistryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    RegistryApi apiInstance = new RegistryApi(defaultClient);
    Integer id = 1; // Integer | Registry entry ID
    try {
      AffiliationDestroy200Response result = apiInstance.registryDestroy(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RegistryApi#registryDestroy");
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
| **id** | **Integer**| Registry entry ID | |

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

<a id="registryIndex"></a>
# **registryIndex**
> RegistryIndex200Response registryIndex()

Registry@index

Return a list of Registry entries

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.RegistryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    RegistryApi apiInstance = new RegistryApi(defaultClient);
    try {
      RegistryIndex200Response result = apiInstance.registryIndex();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RegistryApi#registryIndex");
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

[**RegistryIndex200Response**](RegistryIndex200Response.md)

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

<a id="registryShow"></a>
# **registryShow**
> RegistryIndex200Response registryShow(id)

Registry@show

Return a Registry entry by ID

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.RegistryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    RegistryApi apiInstance = new RegistryApi(defaultClient);
    Integer id = 1; // Integer | Registry entry ID
    try {
      RegistryIndex200Response result = apiInstance.registryShow(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RegistryApi#registryShow");
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
| **id** | **Integer**| Registry entry ID | |

### Return type

[**RegistryIndex200Response**](RegistryIndex200Response.md)

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

<a id="registryStore"></a>
# **registryStore**
> AccreditationStoreByRegistryId201Response registryStore(registry)

Registry@store

Create a Registry entry

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.RegistryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    RegistryApi apiInstance = new RegistryApi(defaultClient);
    Registry registry = new Registry(); // Registry | Registry definition
    try {
      AccreditationStoreByRegistryId201Response result = apiInstance.registryStore(registry);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RegistryApi#registryStore");
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
| **registry** | [**Registry**](Registry.md)| Registry definition | |

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
| **201** | Success |  -  |
| **500** | Error |  -  |

<a id="registryUpdate"></a>
# **registryUpdate**
> RegistryUpdate200Response registryUpdate(id, registry)

Registry@update

Update a Registry entry

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.RegistryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    RegistryApi apiInstance = new RegistryApi(defaultClient);
    Integer id = 1; // Integer | Registry entry ID
    Registry registry = new Registry(); // Registry | Registry definition
    try {
      RegistryUpdate200Response result = apiInstance.registryUpdate(id, registry);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RegistryApi#registryUpdate");
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
| **id** | **Integer**| Registry entry ID | |
| **registry** | [**Registry**](Registry.md)| Registry definition | |

### Return type

[**RegistryUpdate200Response**](RegistryUpdate200Response.md)

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

