# ValidationChecksApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**validationChecksDestroy**](ValidationChecksApi.md#validationChecksDestroy) | **DELETE** /api/v1/validation_checks/{id} | Delete a validation check |
| [**validationChecksIndex**](ValidationChecksApi.md#validationChecksIndex) | **GET** /api/v1/validation_checks | List all validation checks |
| [**validationChecksShow**](ValidationChecksApi.md#validationChecksShow) | **GET** /api/v1/validation_checks/{id} | Get a single validation check |
| [**validationChecksStore**](ValidationChecksApi.md#validationChecksStore) | **POST** /api/v1/validation_checks | Create a new validation check |
| [**validationChecksUpdate**](ValidationChecksApi.md#validationChecksUpdate) | **PUT** /api/v1/validation_checks/{id} | Update a validation check |


<a id="validationChecksDestroy"></a>
# **validationChecksDestroy**
> ValidationChecksDestroy200Response validationChecksDestroy(id)

Delete a validation check

Remove a validation check.

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ValidationChecksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ValidationChecksApi apiInstance = new ValidationChecksApi(defaultClient);
    Integer id = 56; // Integer | ID of the validation check
    try {
      ValidationChecksDestroy200Response result = apiInstance.validationChecksDestroy(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ValidationChecksApi#validationChecksDestroy");
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
| **id** | **Integer**| ID of the validation check | |

### Return type

[**ValidationChecksDestroy200Response**](ValidationChecksDestroy200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Validation check deleted successfully |  -  |
| **400** | Invalid argument(s) |  -  |
| **404** | Validation check not found |  -  |

<a id="validationChecksIndex"></a>
# **validationChecksIndex**
> List&lt;ValidationCheck&gt; validationChecksIndex()

List all validation checks

Retrieve all validation checks.

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ValidationChecksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ValidationChecksApi apiInstance = new ValidationChecksApi(defaultClient);
    try {
      List<ValidationCheck> result = apiInstance.validationChecksIndex();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ValidationChecksApi#validationChecksIndex");
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

[**List&lt;ValidationCheck&gt;**](ValidationCheck.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Validation checks retrieved successfully |  -  |

<a id="validationChecksShow"></a>
# **validationChecksShow**
> ValidationCheck validationChecksShow(id)

Get a single validation check

Retrieve a specific validation check by ID.

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ValidationChecksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ValidationChecksApi apiInstance = new ValidationChecksApi(defaultClient);
    Integer id = 56; // Integer | ID of the validation check
    try {
      ValidationCheck result = apiInstance.validationChecksShow(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ValidationChecksApi#validationChecksShow");
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
| **id** | **Integer**| ID of the validation check | |

### Return type

[**ValidationCheck**](ValidationCheck.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Validation check retrieved successfully |  -  |
| **400** | Invalid argument(s) |  -  |
| **404** | Validation check not found |  -  |

<a id="validationChecksStore"></a>
# **validationChecksStore**
> ValidationCheck validationChecksStore(validationChecksStoreRequest)

Create a new validation check

Create a new validation check entry.

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ValidationChecksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ValidationChecksApi apiInstance = new ValidationChecksApi(defaultClient);
    ValidationChecksStoreRequest validationChecksStoreRequest = new ValidationChecksStoreRequest(); // ValidationChecksStoreRequest | 
    try {
      ValidationCheck result = apiInstance.validationChecksStore(validationChecksStoreRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ValidationChecksApi#validationChecksStore");
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
| **validationChecksStoreRequest** | [**ValidationChecksStoreRequest**](ValidationChecksStoreRequest.md)|  | |

### Return type

[**ValidationCheck**](ValidationCheck.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Validation check created successfully |  -  |

<a id="validationChecksUpdate"></a>
# **validationChecksUpdate**
> ValidationCheck validationChecksUpdate(id, validationChecksStoreRequest)

Update a validation check

Edit an existing validation check.

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ValidationChecksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ValidationChecksApi apiInstance = new ValidationChecksApi(defaultClient);
    Integer id = 56; // Integer | ID of the validation check
    ValidationChecksStoreRequest validationChecksStoreRequest = new ValidationChecksStoreRequest(); // ValidationChecksStoreRequest | 
    try {
      ValidationCheck result = apiInstance.validationChecksUpdate(id, validationChecksStoreRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ValidationChecksApi#validationChecksUpdate");
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
| **id** | **Integer**| ID of the validation check | |
| **validationChecksStoreRequest** | [**ValidationChecksStoreRequest**](ValidationChecksStoreRequest.md)|  | |

### Return type

[**ValidationCheck**](ValidationCheck.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Validation check updated successfully |  -  |
| **400** | Invalid argument(s) |  -  |
| **404** | Validation check not found |  -  |

