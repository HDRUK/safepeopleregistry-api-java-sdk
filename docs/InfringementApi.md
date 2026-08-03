# InfringementApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**infringementIndex**](InfringementApi.md#infringementIndex) | **GET** /api/v1/infringements | Infringement@index |
| [**infringementShow**](InfringementApi.md#infringementShow) | **GET** /api/v1/infringements/{id} | Infringement@show |
| [**infringementStore**](InfringementApi.md#infringementStore) | **POST** /api/v1/infringements | Infringement@store |


<a id="infringementIndex"></a>
# **infringementIndex**
> InfringementIndex200Response infringementIndex()

Infringement@index

Return a list of Infringements

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.InfringementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    InfringementApi apiInstance = new InfringementApi(defaultClient);
    try {
      InfringementIndex200Response result = apiInstance.infringementIndex();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InfringementApi#infringementIndex");
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

[**InfringementIndex200Response**](InfringementIndex200Response.md)

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

<a id="infringementShow"></a>
# **infringementShow**
> InfringementIndex200Response infringementShow(id)

Infringement@show

Return an Infringement entry by ID

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.InfringementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    InfringementApi apiInstance = new InfringementApi(defaultClient);
    Integer id = 1; // Integer | Infringement entry ID
    try {
      InfringementIndex200Response result = apiInstance.infringementShow(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InfringementApi#infringementShow");
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
| **id** | **Integer**| Infringement entry ID | |

### Return type

[**InfringementIndex200Response**](InfringementIndex200Response.md)

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

<a id="infringementStore"></a>
# **infringementStore**
> InfringementStore201Response infringementStore(infringementStoreRequest)

Infringement@store

Create an Infringement entry

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.InfringementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    InfringementApi apiInstance = new InfringementApi(defaultClient);
    InfringementStoreRequest infringementStoreRequest = new InfringementStoreRequest(); // InfringementStoreRequest | Infringement definition
    try {
      InfringementStore201Response result = apiInstance.infringementStore(infringementStoreRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InfringementApi#infringementStore");
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
| **infringementStoreRequest** | [**InfringementStoreRequest**](InfringementStoreRequest.md)| Infringement definition | |

### Return type

[**InfringementStore201Response**](InfringementStore201Response.md)

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

