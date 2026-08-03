# ExperienceApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**experienceDestroy**](ExperienceApi.md#experienceDestroy) | **DELETE** /api/v1/experiences/{id} | Experience@destroy |
| [**experienceIndex**](ExperienceApi.md#experienceIndex) | **GET** /api/v1/experiences | Experience@index |
| [**experienceShow**](ExperienceApi.md#experienceShow) | **GET** /api/v1/experiences/{id} | Experience@show |
| [**experienceStore**](ExperienceApi.md#experienceStore) | **POST** /api/v1/experiences | Experience@store |
| [**experienceUpdate**](ExperienceApi.md#experienceUpdate) | **PUT** /api/v1/experiences/{id} | Experience@update |


<a id="experienceDestroy"></a>
# **experienceDestroy**
> AffiliationDestroy200Response experienceDestroy(id)

Experience@destroy

Delete a Experience entry from the system

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ExperienceApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ExperienceApi apiInstance = new ExperienceApi(defaultClient);
    Integer id = 1; // Integer | Experience entry ID
    try {
      AffiliationDestroy200Response result = apiInstance.experienceDestroy(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ExperienceApi#experienceDestroy");
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
| **id** | **Integer**| Experience entry ID | |

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

<a id="experienceIndex"></a>
# **experienceIndex**
> ExperienceIndex200Response experienceIndex()

Experience@index

Return a list of Experience entries

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ExperienceApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ExperienceApi apiInstance = new ExperienceApi(defaultClient);
    try {
      ExperienceIndex200Response result = apiInstance.experienceIndex();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ExperienceApi#experienceIndex");
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

[**ExperienceIndex200Response**](ExperienceIndex200Response.md)

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

<a id="experienceShow"></a>
# **experienceShow**
> ExperienceShow200Response experienceShow(id)

Experience@show

Return an Experience entry by ID

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ExperienceApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ExperienceApi apiInstance = new ExperienceApi(defaultClient);
    Integer id = 1; // Integer | Experience entry ID
    try {
      ExperienceShow200Response result = apiInstance.experienceShow(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ExperienceApi#experienceShow");
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
| **id** | **Integer**| Experience entry ID | |

### Return type

[**ExperienceShow200Response**](ExperienceShow200Response.md)

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

<a id="experienceStore"></a>
# **experienceStore**
> ExperienceStore201Response experienceStore(experienceStoreRequest)

Experience@store

Create an Experience entry

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ExperienceApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ExperienceApi apiInstance = new ExperienceApi(defaultClient);
    ExperienceStoreRequest experienceStoreRequest = new ExperienceStoreRequest(); // ExperienceStoreRequest | Experience definition
    try {
      ExperienceStore201Response result = apiInstance.experienceStore(experienceStoreRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ExperienceApi#experienceStore");
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
| **experienceStoreRequest** | [**ExperienceStoreRequest**](ExperienceStoreRequest.md)| Experience definition | |

### Return type

[**ExperienceStore201Response**](ExperienceStore201Response.md)

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

<a id="experienceUpdate"></a>
# **experienceUpdate**
> ExperienceUpdate200Response experienceUpdate(id, experienceStoreRequest)

Experience@update

Update an Experience entry

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ExperienceApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ExperienceApi apiInstance = new ExperienceApi(defaultClient);
    Integer id = 1; // Integer | Experience entry ID
    ExperienceStoreRequest experienceStoreRequest = new ExperienceStoreRequest(); // ExperienceStoreRequest | Experience definition
    try {
      ExperienceUpdate200Response result = apiInstance.experienceUpdate(id, experienceStoreRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ExperienceApi#experienceUpdate");
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
| **id** | **Integer**| Experience entry ID | |
| **experienceStoreRequest** | [**ExperienceStoreRequest**](ExperienceStoreRequest.md)| Experience definition | |

### Return type

[**ExperienceUpdate200Response**](ExperienceUpdate200Response.md)

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

