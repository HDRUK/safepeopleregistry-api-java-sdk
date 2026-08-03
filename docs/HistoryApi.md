# HistoryApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**historyIndex**](HistoryApi.md#historyIndex) | **GET** /api/v1/histories | History@index |
| [**historyShow**](HistoryApi.md#historyShow) | **GET** /api/v1/histories/{id} | History@show |
| [**historyStore**](HistoryApi.md#historyStore) | **POST** /api/v1/histories | History@store |


<a id="historyIndex"></a>
# **historyIndex**
> HistoryIndex200Response historyIndex()

History@index

Return a list of Histories

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.HistoryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    HistoryApi apiInstance = new HistoryApi(defaultClient);
    try {
      HistoryIndex200Response result = apiInstance.historyIndex();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling HistoryApi#historyIndex");
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

[**HistoryIndex200Response**](HistoryIndex200Response.md)

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

<a id="historyShow"></a>
# **historyShow**
> HistoryIndex200Response historyShow(id)

History@show

Return a History entry by ID

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.HistoryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    HistoryApi apiInstance = new HistoryApi(defaultClient);
    Integer id = 1; // Integer | History entry ID
    try {
      HistoryIndex200Response result = apiInstance.historyShow(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling HistoryApi#historyShow");
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
| **id** | **Integer**| History entry ID | |

### Return type

[**HistoryIndex200Response**](HistoryIndex200Response.md)

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

<a id="historyStore"></a>
# **historyStore**
> HistoryStore201Response historyStore(historyStoreRequest)

History@store

Create a History entry

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.HistoryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    HistoryApi apiInstance = new HistoryApi(defaultClient);
    HistoryStoreRequest historyStoreRequest = new HistoryStoreRequest(); // HistoryStoreRequest | History definition
    try {
      HistoryStore201Response result = apiInstance.historyStore(historyStoreRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling HistoryApi#historyStore");
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
| **historyStoreRequest** | [**HistoryStoreRequest**](HistoryStoreRequest.md)| History definition | |

### Return type

[**HistoryStore201Response**](HistoryStore201Response.md)

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

