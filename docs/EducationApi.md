# EducationApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**educationDestroyByRegistryId**](EducationApi.md#educationDestroyByRegistryId) | **DELETE** /api/v1/registries/{registryId}/educations/{id} | Delete an education record |
| [**educationIndexByRegistryId**](EducationApi.md#educationIndexByRegistryId) | **GET** /api/v1/educations/registries/{registryId} | Get education records by registry ID |
| [**educationShowByRegistryId**](EducationApi.md#educationShowByRegistryId) | **GET** /api/v1/educations/{id}/registries/{registryId} | Get a specific education record by ID and registry ID |
| [**educationStoreByRegistryId**](EducationApi.md#educationStoreByRegistryId) | **POST** /api/v1/registries/{registryId}/educations | Create a new education record for a registry |
| [**educationUpdateByRegistryId**](EducationApi.md#educationUpdateByRegistryId) | **PUT** /api/v1/registries/{registryId}/educations/{id} | Update an existing education record |


<a id="educationDestroyByRegistryId"></a>
# **educationDestroyByRegistryId**
> EducationDestroyByRegistryId200Response educationDestroyByRegistryId(registryId, id)

Delete an education record

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.EducationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    EducationApi apiInstance = new EducationApi(defaultClient);
    Integer registryId = 1; // Integer | ID of the registry
    Integer id = 1; // Integer | ID of the education record
    try {
      EducationDestroyByRegistryId200Response result = apiInstance.educationDestroyByRegistryId(registryId, id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EducationApi#educationDestroyByRegistryId");
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
| **registryId** | **Integer**| ID of the registry | |
| **id** | **Integer**| ID of the education record | |

### Return type

[**EducationDestroyByRegistryId200Response**](EducationDestroyByRegistryId200Response.md)

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

<a id="educationIndexByRegistryId"></a>
# **educationIndexByRegistryId**
> List&lt;Education&gt; educationIndexByRegistryId(registryId)

Get education records by registry ID

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.EducationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    EducationApi apiInstance = new EducationApi(defaultClient);
    Integer registryId = 1; // Integer | ID of the registry
    try {
      List<Education> result = apiInstance.educationIndexByRegistryId(registryId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EducationApi#educationIndexByRegistryId");
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
| **registryId** | **Integer**| ID of the registry | |

### Return type

[**List&lt;Education&gt;**](Education.md)

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

<a id="educationShowByRegistryId"></a>
# **educationShowByRegistryId**
> Education educationShowByRegistryId(registryId, id)

Get a specific education record by ID and registry ID

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.EducationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    EducationApi apiInstance = new EducationApi(defaultClient);
    Integer registryId = 1; // Integer | ID of the registry
    Integer id = 1; // Integer | ID of the education record
    try {
      Education result = apiInstance.educationShowByRegistryId(registryId, id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EducationApi#educationShowByRegistryId");
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
| **registryId** | **Integer**| ID of the registry | |
| **id** | **Integer**| ID of the education record | |

### Return type

[**Education**](Education.md)

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
| **404** | Education record not found |  -  |

<a id="educationStoreByRegistryId"></a>
# **educationStoreByRegistryId**
> AccreditationStoreByRegistryId201Response educationStoreByRegistryId(registryId, education)

Create a new education record for a registry

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.EducationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    EducationApi apiInstance = new EducationApi(defaultClient);
    Integer registryId = 1; // Integer | ID of the registry
    Education education = new Education(); // Education | 
    try {
      AccreditationStoreByRegistryId201Response result = apiInstance.educationStoreByRegistryId(registryId, education);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EducationApi#educationStoreByRegistryId");
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
| **registryId** | **Integer**| ID of the registry | |
| **education** | [**Education**](Education.md)|  | |

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
| **400** | Invalid argument(s) |  -  |

<a id="educationUpdateByRegistryId"></a>
# **educationUpdateByRegistryId**
> Education educationUpdateByRegistryId(registryId, id, education)

Update an existing education record

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.EducationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    EducationApi apiInstance = new EducationApi(defaultClient);
    Integer registryId = 1; // Integer | ID of the registry
    Integer id = 1; // Integer | ID of the education record
    Education education = new Education(); // Education | 
    try {
      Education result = apiInstance.educationUpdateByRegistryId(registryId, id, education);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EducationApi#educationUpdateByRegistryId");
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
| **registryId** | **Integer**| ID of the registry | |
| **id** | **Integer**| ID of the education record | |
| **education** | [**Education**](Education.md)|  | |

### Return type

[**Education**](Education.md)

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

