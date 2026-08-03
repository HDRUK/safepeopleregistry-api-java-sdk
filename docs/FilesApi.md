# FilesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**filesDownload**](FilesApi.md#filesDownload) | **GET** /api/v1/files/{id}/download | Download an uploaded file |
| [**filesShow**](FilesApi.md#filesShow) | **GET** /api/v1/files/{id} | Files@show |
| [**filesStore**](FilesApi.md#filesStore) | **POST** /api/v1/files | Files@store |


<a id="filesDownload"></a>
# **filesDownload**
> File filesDownload(id)

Download an uploaded file

Downloads the specified file

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.FilesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    FilesApi apiInstance = new FilesApi(defaultClient);
    Integer id = 1; // Integer | File ID
    try {
      File result = apiInstance.filesDownload(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FilesApi#filesDownload");
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
| **id** | **Integer**| File ID | |

### Return type

[**File**](File.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/octet-stream, application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | File downloaded successfully |  -  |
| **400** | Invalid argument(s) |  -  |
| **404** | File not found |  -  |

<a id="filesShow"></a>
# **filesShow**
> FilesShow200Response filesShow(id)

Files@show

Gets an uploaded file

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.FilesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    FilesApi apiInstance = new FilesApi(defaultClient);
    Integer id = 1; // Integer | File ID
    try {
      FilesShow200Response result = apiInstance.filesShow(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FilesApi#filesShow");
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
| **id** | **Integer**| File ID | |

### Return type

[**FilesShow200Response**](FilesShow200Response.md)

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
| **404** | Not found |  -  |

<a id="filesStore"></a>
# **filesStore**
> AccreditationStoreByRegistryId201Response filesStore(registryId, _file, fileType, entityType)

Files@store

Uploads a file to the registry

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.FilesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    FilesApi apiInstance = new FilesApi(defaultClient);
    Integer registryId = 56; // Integer | 
    File _file = new File("/path/to/file"); // File | 
    String fileType = "fileType_example"; // String | 
    String entityType = "entityType_example"; // String | 
    try {
      AccreditationStoreByRegistryId201Response result = apiInstance.filesStore(registryId, _file, fileType, entityType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FilesApi#filesStore");
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
| **registryId** | **Integer**|  | [optional] |
| **_file** | **File**|  | [optional] |
| **fileType** | **String**|  | [optional] |
| **entityType** | **String**|  | [optional] |

### Return type

[**AccreditationStoreByRegistryId201Response**](AccreditationStoreByRegistryId201Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **400** | Bad request |  -  |
| **201** | Success |  -  |

