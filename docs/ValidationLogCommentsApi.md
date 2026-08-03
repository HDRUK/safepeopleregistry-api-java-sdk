# ValidationLogCommentsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**validationLogCommentsComments**](ValidationLogCommentsApi.md#validationLogCommentsComments) | **GET** /api/v1/validation_logs/{id}/comments | Get all comments for a Validation Log |
| [**validationLogCommentsDestroy**](ValidationLogCommentsApi.md#validationLogCommentsDestroy) | **DELETE** /api/v1/validation_log_comments/{id} | Delete a validation log comment |
| [**validationLogCommentsShow**](ValidationLogCommentsApi.md#validationLogCommentsShow) | **GET** /api/v1/validation_log_comments/{id} | Get a single validation log comment |
| [**validationLogCommentsStore**](ValidationLogCommentsApi.md#validationLogCommentsStore) | **POST** /api/v1/validation_log_comments | Create a new validation log comment |
| [**validationLogCommentsUpdate**](ValidationLogCommentsApi.md#validationLogCommentsUpdate) | **PUT** /api/v1/validation_log_comments/{id} | Update a validation log comment |


<a id="validationLogCommentsComments"></a>
# **validationLogCommentsComments**
> List&lt;ValidationLog&gt; validationLogCommentsComments(id)

Get all comments for a Validation Log

Retrieve all comments associated with a specific validation log entry.

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ValidationLogCommentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ValidationLogCommentsApi apiInstance = new ValidationLogCommentsApi(defaultClient);
    Integer id = 56; // Integer | The ID of the validation log
    try {
      List<ValidationLog> result = apiInstance.validationLogCommentsComments(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ValidationLogCommentsApi#validationLogCommentsComments");
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
| **id** | **Integer**| The ID of the validation log | |

### Return type

[**List&lt;ValidationLog&gt;**](ValidationLog.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Validation log with comments |  -  |
| **404** | Validation log not found |  -  |

<a id="validationLogCommentsDestroy"></a>
# **validationLogCommentsDestroy**
> ValidationLogCommentsDestroy200Response validationLogCommentsDestroy(id)

Delete a validation log comment

Remove a comment from the validation logs.

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ValidationLogCommentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ValidationLogCommentsApi apiInstance = new ValidationLogCommentsApi(defaultClient);
    Integer id = 56; // Integer | The ID of the comment
    try {
      ValidationLogCommentsDestroy200Response result = apiInstance.validationLogCommentsDestroy(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ValidationLogCommentsApi#validationLogCommentsDestroy");
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
| **id** | **Integer**| The ID of the comment | |

### Return type

[**ValidationLogCommentsDestroy200Response**](ValidationLogCommentsDestroy200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Comment deleted successfully |  -  |
| **400** | Comment not found |  -  |
| **404** | Comment not found |  -  |

<a id="validationLogCommentsShow"></a>
# **validationLogCommentsShow**
> ValidationLogComment validationLogCommentsShow(id)

Get a single validation log comment

Retrieve a specific validation log comment by ID.

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ValidationLogCommentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ValidationLogCommentsApi apiInstance = new ValidationLogCommentsApi(defaultClient);
    Integer id = 56; // Integer | The ID of the comment
    try {
      ValidationLogComment result = apiInstance.validationLogCommentsShow(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ValidationLogCommentsApi#validationLogCommentsShow");
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
| **id** | **Integer**| The ID of the comment | |

### Return type

[**ValidationLogComment**](ValidationLogComment.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Comment retrieved successfully |  -  |
| **400** | Comment not found |  -  |
| **404** | Comment not found |  -  |

<a id="validationLogCommentsStore"></a>
# **validationLogCommentsStore**
> ValidationLogComment validationLogCommentsStore(validationLogCommentsStoreRequest)

Create a new validation log comment

Add a new comment to a validation log.

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ValidationLogCommentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ValidationLogCommentsApi apiInstance = new ValidationLogCommentsApi(defaultClient);
    ValidationLogCommentsStoreRequest validationLogCommentsStoreRequest = new ValidationLogCommentsStoreRequest(); // ValidationLogCommentsStoreRequest | 
    try {
      ValidationLogComment result = apiInstance.validationLogCommentsStore(validationLogCommentsStoreRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ValidationLogCommentsApi#validationLogCommentsStore");
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
| **validationLogCommentsStoreRequest** | [**ValidationLogCommentsStoreRequest**](ValidationLogCommentsStoreRequest.md)|  | |

### Return type

[**ValidationLogComment**](ValidationLogComment.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Comment created successfully |  -  |

<a id="validationLogCommentsUpdate"></a>
# **validationLogCommentsUpdate**
> ValidationLogComment validationLogCommentsUpdate(id, validationLogCommentsUpdateRequest)

Update a validation log comment

Edit an existing validation log comment.

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ValidationLogCommentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ValidationLogCommentsApi apiInstance = new ValidationLogCommentsApi(defaultClient);
    Integer id = 56; // Integer | The ID of the comment
    ValidationLogCommentsUpdateRequest validationLogCommentsUpdateRequest = new ValidationLogCommentsUpdateRequest(); // ValidationLogCommentsUpdateRequest | 
    try {
      ValidationLogComment result = apiInstance.validationLogCommentsUpdate(id, validationLogCommentsUpdateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ValidationLogCommentsApi#validationLogCommentsUpdate");
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
| **id** | **Integer**| The ID of the comment | |
| **validationLogCommentsUpdateRequest** | [**ValidationLogCommentsUpdateRequest**](ValidationLogCommentsUpdateRequest.md)|  | |

### Return type

[**ValidationLogComment**](ValidationLogComment.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Comment updated successfully |  -  |
| **400** | Comment not found |  -  |
| **404** | Comment not found |  -  |

