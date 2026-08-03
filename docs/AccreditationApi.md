# AccreditationApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**accreditationIndexByRegistryId**](AccreditationApi.md#accreditationIndexByRegistryId) | **GET** /api/v1/accreditations/{registryId} | Get accreditations by registry ID |
| [**accreditationStoreByRegistryId**](AccreditationApi.md#accreditationStoreByRegistryId) | **POST** /api/v1/accreditations/{registryId} | Create accreditation for a registry |
| [**accreditationUpdateByRegistryId**](AccreditationApi.md#accreditationUpdateByRegistryId) | **PUT** /api/v1/accreditations/{id}/registries/{registryId} | Update accreditation for a registry |


<a id="accreditationIndexByRegistryId"></a>
# **accreditationIndexByRegistryId**
> AccreditationIndexByRegistryId200Response accreditationIndexByRegistryId(registryId)

Get accreditations by registry ID

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.AccreditationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    AccreditationApi apiInstance = new AccreditationApi(defaultClient);
    Integer registryId = 1; // Integer | ID of the registry
    try {
      AccreditationIndexByRegistryId200Response result = apiInstance.accreditationIndexByRegistryId(registryId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AccreditationApi#accreditationIndexByRegistryId");
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

[**AccreditationIndexByRegistryId200Response**](AccreditationIndexByRegistryId200Response.md)

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

<a id="accreditationStoreByRegistryId"></a>
# **accreditationStoreByRegistryId**
> AccreditationStoreByRegistryId201Response accreditationStoreByRegistryId(registryId, accreditation)

Create accreditation for a registry

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.AccreditationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    AccreditationApi apiInstance = new AccreditationApi(defaultClient);
    Integer registryId = 1; // Integer | ID of the registry
    Accreditation accreditation = new Accreditation(); // Accreditation | 
    try {
      AccreditationStoreByRegistryId201Response result = apiInstance.accreditationStoreByRegistryId(registryId, accreditation);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AccreditationApi#accreditationStoreByRegistryId");
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
| **accreditation** | [**Accreditation**](Accreditation.md)|  | |

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

<a id="accreditationUpdateByRegistryId"></a>
# **accreditationUpdateByRegistryId**
> AccreditationUpdateByRegistryId200Response accreditationUpdateByRegistryId(registryId, id, accreditation)

Update accreditation for a registry

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.AccreditationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    AccreditationApi apiInstance = new AccreditationApi(defaultClient);
    Integer registryId = 1; // Integer | ID of the registry
    Integer id = 1; // Integer | ID of the accreditation
    Accreditation accreditation = new Accreditation(); // Accreditation | 
    try {
      AccreditationUpdateByRegistryId200Response result = apiInstance.accreditationUpdateByRegistryId(registryId, id, accreditation);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AccreditationApi#accreditationUpdateByRegistryId");
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
| **id** | **Integer**| ID of the accreditation | |
| **accreditation** | [**Accreditation**](Accreditation.md)|  | |

### Return type

[**AccreditationUpdateByRegistryId200Response**](AccreditationUpdateByRegistryId200Response.md)

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

