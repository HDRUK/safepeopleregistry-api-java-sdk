# ResolutionApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**resolutionIndexByRegistryId**](ResolutionApi.md#resolutionIndexByRegistryId) | **GET** /api/v1/registries/{registryId}/resolutions | Get resolutions by registry ID |
| [**resolutionStoreByRegistryId**](ResolutionApi.md#resolutionStoreByRegistryId) | **POST** /api/v1/registries/{registryId}/resolutions | Create a new resolution for a registry |


<a id="resolutionIndexByRegistryId"></a>
# **resolutionIndexByRegistryId**
> List&lt;Resolution&gt; resolutionIndexByRegistryId(registryId)

Get resolutions by registry ID

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ResolutionApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ResolutionApi apiInstance = new ResolutionApi(defaultClient);
    Integer registryId = 1; // Integer | ID of the registry
    try {
      List<Resolution> result = apiInstance.resolutionIndexByRegistryId(registryId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResolutionApi#resolutionIndexByRegistryId");
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

[**List&lt;Resolution&gt;**](Resolution.md)

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

<a id="resolutionStoreByRegistryId"></a>
# **resolutionStoreByRegistryId**
> AccreditationStoreByRegistryId201Response resolutionStoreByRegistryId(registryId, resolution)

Create a new resolution for a registry

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ResolutionApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ResolutionApi apiInstance = new ResolutionApi(defaultClient);
    Integer registryId = 1; // Integer | ID of the registry
    Resolution resolution = new Resolution(); // Resolution | 
    try {
      AccreditationStoreByRegistryId201Response result = apiInstance.resolutionStoreByRegistryId(registryId, resolution);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResolutionApi#resolutionStoreByRegistryId");
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
| **resolution** | [**Resolution**](Resolution.md)|  | |

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

