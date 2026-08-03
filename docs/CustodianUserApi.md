# CustodianUserApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**custodianUserBulkStore**](CustodianUserApi.md#custodianUserBulkStore) | **POST** /api/v1/custodian_users/bulk | Create multiple CustodianUser entries |
| [**custodianUserDestroy**](CustodianUserApi.md#custodianUserDestroy) | **DELETE** /api/v1/custodian_users/{id} | CustodianUser@destroy |
| [**custodianUserShow**](CustodianUserApi.md#custodianUserShow) | **GET** /api/v1/custodian_users/{id} | CustodianUser@show |
| [**custodianUserStore**](CustodianUserApi.md#custodianUserStore) | **POST** /api/v1/custodian_users | CustodianUser@store |
| [**custodianUserUpdate**](CustodianUserApi.md#custodianUserUpdate) | **PUT** /api/v1/custodian_users | CustodianUser@update |


<a id="custodianUserBulkStore"></a>
# **custodianUserBulkStore**
> CustodianUserBulkStore201Response custodianUserBulkStore(custodianUserBulkStoreRequest)

Create multiple CustodianUser entries

Create multiple CustodianUser entries

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.CustodianUserApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CustodianUserApi apiInstance = new CustodianUserApi(defaultClient);
    CustodianUserBulkStoreRequest custodianUserBulkStoreRequest = new CustodianUserBulkStoreRequest(); // CustodianUserBulkStoreRequest | Array of CustodianUser definitions
    try {
      CustodianUserBulkStore201Response result = apiInstance.custodianUserBulkStore(custodianUserBulkStoreRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustodianUserApi#custodianUserBulkStore");
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
| **custodianUserBulkStoreRequest** | [**CustodianUserBulkStoreRequest**](CustodianUserBulkStoreRequest.md)| Array of CustodianUser definitions | |

### Return type

[**CustodianUserBulkStore201Response**](CustodianUserBulkStore201Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Success |  -  |
| **500** | Error |  -  |

<a id="custodianUserDestroy"></a>
# **custodianUserDestroy**
> AffiliationDestroy200Response custodianUserDestroy(id)

CustodianUser@destroy

Delete a CustodianUser entry from the system

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.CustodianUserApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CustodianUserApi apiInstance = new CustodianUserApi(defaultClient);
    Integer id = 1; // Integer | CustodianUser entry ID
    try {
      AffiliationDestroy200Response result = apiInstance.custodianUserDestroy(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustodianUserApi#custodianUserDestroy");
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
| **id** | **Integer**| CustodianUser entry ID | |

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
| **400** | Invalid argument(s) |  -  |
| **404** | Not found response |  -  |
| **200** | Success |  -  |
| **500** | Error |  -  |

<a id="custodianUserShow"></a>
# **custodianUserShow**
> CustodianUserShow200Response custodianUserShow(id)

CustodianUser@show

Return a CustodianUser entry by ID

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.CustodianUserApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CustodianUserApi apiInstance = new CustodianUserApi(defaultClient);
    Integer id = 1; // Integer | CustodianUser entry ID
    try {
      CustodianUserShow200Response result = apiInstance.custodianUserShow(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustodianUserApi#custodianUserShow");
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
| **id** | **Integer**| CustodianUser entry ID | |

### Return type

[**CustodianUserShow200Response**](CustodianUserShow200Response.md)

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

<a id="custodianUserStore"></a>
# **custodianUserStore**
> AccreditationStoreByRegistryId201Response custodianUserStore(custodianUser)

CustodianUser@store

Create a CustodianUser entry

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.CustodianUserApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CustodianUserApi apiInstance = new CustodianUserApi(defaultClient);
    CustodianUser custodianUser = new CustodianUser(); // CustodianUser | CustodianUser definition
    try {
      AccreditationStoreByRegistryId201Response result = apiInstance.custodianUserStore(custodianUser);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustodianUserApi#custodianUserStore");
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
| **custodianUser** | [**CustodianUser**](CustodianUser.md)| CustodianUser definition | |

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

<a id="custodianUserUpdate"></a>
# **custodianUserUpdate**
> CustodianUserUpdate201Response custodianUserUpdate(custodianUser)

CustodianUser@update

Update a CustodianUser entry

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.CustodianUserApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CustodianUserApi apiInstance = new CustodianUserApi(defaultClient);
    CustodianUser custodianUser = new CustodianUser(); // CustodianUser | CustodianUser definition
    try {
      CustodianUserUpdate201Response result = apiInstance.custodianUserUpdate(custodianUser);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustodianUserApi#custodianUserUpdate");
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
| **custodianUser** | [**CustodianUser**](CustodianUser.md)| CustodianUser definition | |

### Return type

[**CustodianUserUpdate201Response**](CustodianUserUpdate201Response.md)

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
| **400** | Invalid argument(s) |  -  |
| **500** | Error |  -  |

