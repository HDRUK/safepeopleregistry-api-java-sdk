# TrainingApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**trainingIndex**](TrainingApi.md#trainingIndex) | **GET** /api/v1/training | Training@index |
| [**trainingIndexByRegistryId**](TrainingApi.md#trainingIndexByRegistryId) | **GET** /api/v1/training/registry/{id} | Training@show |
| [**trainingShow**](TrainingApi.md#trainingShow) | **GET** /api/v1/training/{id} | Training@show |
| [**trainingStore**](TrainingApi.md#trainingStore) | **POST** /api/v1/training | Training@store |
| [**trainingUpdate**](TrainingApi.md#trainingUpdate) | **PUT** /api/v1/training/{id} | Training@update |


<a id="trainingIndex"></a>
# **trainingIndex**
> TrainingShow200Response trainingIndex()

Training@index

Return a list of Training entries

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.TrainingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    TrainingApi apiInstance = new TrainingApi(defaultClient);
    try {
      TrainingShow200Response result = apiInstance.trainingIndex();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TrainingApi#trainingIndex");
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

[**TrainingShow200Response**](TrainingShow200Response.md)

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

<a id="trainingIndexByRegistryId"></a>
# **trainingIndexByRegistryId**
> TrainingShow200Response trainingIndexByRegistryId(id)

Training@show

Return a list of training by registry id

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.TrainingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    TrainingApi apiInstance = new TrainingApi(defaultClient);
    Integer id = 1; // Integer | Training registry id
    try {
      TrainingShow200Response result = apiInstance.trainingIndexByRegistryId(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TrainingApi#trainingIndexByRegistryId");
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
| **id** | **Integer**| Training registry id | |

### Return type

[**TrainingShow200Response**](TrainingShow200Response.md)

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

<a id="trainingShow"></a>
# **trainingShow**
> TrainingShow200Response trainingShow(id)

Training@show

Return a training record by registry id

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.TrainingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    TrainingApi apiInstance = new TrainingApi(defaultClient);
    Integer id = 1; // Integer | Training id
    try {
      TrainingShow200Response result = apiInstance.trainingShow(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TrainingApi#trainingShow");
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
| **id** | **Integer**| Training id | |

### Return type

[**TrainingShow200Response**](TrainingShow200Response.md)

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

<a id="trainingStore"></a>
# **trainingStore**
> AccreditationStoreByRegistryId201Response trainingStore(training)

Training@store

Create a Training entry

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.TrainingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    TrainingApi apiInstance = new TrainingApi(defaultClient);
    Training training = new Training(); // Training | Training definition
    try {
      AccreditationStoreByRegistryId201Response result = apiInstance.trainingStore(training);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TrainingApi#trainingStore");
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
| **training** | [**Training**](Training.md)| Training definition | |

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

<a id="trainingUpdate"></a>
# **trainingUpdate**
> TrainingUpdate200Response trainingUpdate(id, training)

Training@update

Update a Training entry

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.TrainingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    TrainingApi apiInstance = new TrainingApi(defaultClient);
    Integer id = 1; // Integer | Training entry ID
    Training training = new Training(); // Training | Training definition
    try {
      TrainingUpdate200Response result = apiInstance.trainingUpdate(id, training);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TrainingApi#trainingUpdate");
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
| **id** | **Integer**| Training entry ID | |
| **training** | [**Training**](Training.md)| Training definition | |

### Return type

[**TrainingUpdate200Response**](TrainingUpdate200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **400** | Invalid argument(s) |  -  |
| **404** | Not found response |  -  |
| **200** | Success |  -  |
| **500** | Error |  -  |

