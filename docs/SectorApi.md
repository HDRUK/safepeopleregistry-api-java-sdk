# SectorApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**sectorDestroy**](SectorApi.md#sectorDestroy) | **DELETE** /api/v1/sectors/{id} | Delete a sector |
| [**sectorIndex**](SectorApi.md#sectorIndex) | **GET** /api/v1/sectors | Get a list of sectors |
| [**sectorShow**](SectorApi.md#sectorShow) | **GET** /api/v1/sectors/{id} | Get a specific sector by ID |
| [**sectorStore**](SectorApi.md#sectorStore) | **POST** /api/v1/sectors | Create a new sector |
| [**sectorUpdate**](SectorApi.md#sectorUpdate) | **PUT** /api/v1/sectors/{id} | Update an existing sector |


<a id="sectorDestroy"></a>
# **sectorDestroy**
> AffiliationDestroy200Response sectorDestroy(id)

Delete a sector

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.SectorApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    SectorApi apiInstance = new SectorApi(defaultClient);
    Integer id = 1; // Integer | ID of the sector
    try {
      AffiliationDestroy200Response result = apiInstance.sectorDestroy(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SectorApi#sectorDestroy");
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
| **id** | **Integer**| ID of the sector | |

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
| **404** | Sector not found |  -  |

<a id="sectorIndex"></a>
# **sectorIndex**
> List&lt;Sector&gt; sectorIndex()

Get a list of sectors

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.SectorApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    SectorApi apiInstance = new SectorApi(defaultClient);
    try {
      List<Sector> result = apiInstance.sectorIndex();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SectorApi#sectorIndex");
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

[**List&lt;Sector&gt;**](Sector.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

<a id="sectorShow"></a>
# **sectorShow**
> Sector sectorShow(id)

Get a specific sector by ID

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.SectorApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    SectorApi apiInstance = new SectorApi(defaultClient);
    Integer id = 1; // Integer | ID of the sector
    try {
      Sector result = apiInstance.sectorShow(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SectorApi#sectorShow");
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
| **id** | **Integer**| ID of the sector | |

### Return type

[**Sector**](Sector.md)

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
| **404** | Sector not found |  -  |

<a id="sectorStore"></a>
# **sectorStore**
> AccreditationStoreByRegistryId201Response sectorStore(sector)

Create a new sector

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.SectorApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    SectorApi apiInstance = new SectorApi(defaultClient);
    Sector sector = new Sector(); // Sector | 
    try {
      AccreditationStoreByRegistryId201Response result = apiInstance.sectorStore(sector);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SectorApi#sectorStore");
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
| **sector** | [**Sector**](Sector.md)|  | |

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

<a id="sectorUpdate"></a>
# **sectorUpdate**
> Sector sectorUpdate(id, sector)

Update an existing sector

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.SectorApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    SectorApi apiInstance = new SectorApi(defaultClient);
    Integer id = 1; // Integer | ID of the sector
    Sector sector = new Sector(); // Sector | 
    try {
      Sector result = apiInstance.sectorUpdate(id, sector);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SectorApi#sectorUpdate");
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
| **id** | **Integer**| ID of the sector | |
| **sector** | [**Sector**](Sector.md)|  | |

### Return type

[**Sector**](Sector.md)

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
| **404** | Sector not found |  -  |

