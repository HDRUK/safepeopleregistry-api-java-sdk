# IdentityApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**identityDestroy**](IdentityApi.md#identityDestroy) | **DELETE** /api/v1/identities/{id} | Identity@destroy |
| [**identityIndex**](IdentityApi.md#identityIndex) | **GET** /api/v1/identities | Identity@index |
| [**identityShow**](IdentityApi.md#identityShow) | **GET** /api/v1/identities/{id} | Identity@show |
| [**identityStore**](IdentityApi.md#identityStore) | **POST** /api/v1/identities | Identity@store |
| [**identityUpdate**](IdentityApi.md#identityUpdate) | **PUT** /api/v1/identities/{id} | Identity@update |


<a id="identityDestroy"></a>
# **identityDestroy**
> AffiliationDestroy200Response identityDestroy(id)

Identity@destroy

Delete an Identity entry from the system

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.IdentityApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    IdentityApi apiInstance = new IdentityApi(defaultClient);
    Integer id = 1; // Integer | Identity entry ID
    try {
      AffiliationDestroy200Response result = apiInstance.identityDestroy(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling IdentityApi#identityDestroy");
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
| **id** | **Integer**| Identity entry ID | |

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

<a id="identityIndex"></a>
# **identityIndex**
> IdentityIndex200Response identityIndex()

Identity@index

Return a list of Identity entries

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.IdentityApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    IdentityApi apiInstance = new IdentityApi(defaultClient);
    try {
      IdentityIndex200Response result = apiInstance.identityIndex();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling IdentityApi#identityIndex");
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

[**IdentityIndex200Response**](IdentityIndex200Response.md)

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

<a id="identityShow"></a>
# **identityShow**
> IdentityIndex200Response identityShow(id)

Identity@show

Return an Identity entry by ID

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.IdentityApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    IdentityApi apiInstance = new IdentityApi(defaultClient);
    Integer id = 1; // Integer | Identity ID
    try {
      IdentityIndex200Response result = apiInstance.identityShow(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling IdentityApi#identityShow");
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
| **id** | **Integer**| Identity ID | |

### Return type

[**IdentityIndex200Response**](IdentityIndex200Response.md)

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

<a id="identityStore"></a>
# **identityStore**
> IdentityStore201Response identityStore(identityStoreRequest)

Identity@store

Create a Identity entry

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.IdentityApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    IdentityApi apiInstance = new IdentityApi(defaultClient);
    IdentityStoreRequest identityStoreRequest = new IdentityStoreRequest(); // IdentityStoreRequest | Identity definition
    try {
      IdentityStore201Response result = apiInstance.identityStore(identityStoreRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling IdentityApi#identityStore");
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
| **identityStoreRequest** | [**IdentityStoreRequest**](IdentityStoreRequest.md)| Identity definition | |

### Return type

[**IdentityStore201Response**](IdentityStore201Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Success |  -  |
| **404** | Not found response |  -  |
| **500** | Error |  -  |

<a id="identityUpdate"></a>
# **identityUpdate**
> IdentityUpdate200Response identityUpdate(id, identityStoreRequest)

Identity@update

Update a Identity entry

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.IdentityApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    IdentityApi apiInstance = new IdentityApi(defaultClient);
    Integer id = 1; // Integer | Identity entry ID
    IdentityStoreRequest identityStoreRequest = new IdentityStoreRequest(); // IdentityStoreRequest | Identity definition
    try {
      IdentityUpdate200Response result = apiInstance.identityUpdate(id, identityStoreRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling IdentityApi#identityUpdate");
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
| **id** | **Integer**| Identity entry ID | |
| **identityStoreRequest** | [**IdentityStoreRequest**](IdentityStoreRequest.md)| Identity definition | |

### Return type

[**IdentityUpdate200Response**](IdentityUpdate200Response.md)

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

