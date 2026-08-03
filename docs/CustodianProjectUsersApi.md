# CustodianProjectUsersApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**custodianProjectUsersIndex**](CustodianProjectUsersApi.md#custodianProjectUsersIndex) | **GET** /api/v1/custodian_approvals/{custodianId}/projectUsers | List all project users associated with a custodian |
| [**custodianProjectUsersShow**](CustodianProjectUsersApi.md#custodianProjectUsersShow) | **GET** /api/v1/custodian_approvals/{custodianId}/projectUsers/{projectUserId} | Get custodian approval for a project user |
| [**custodianProjectUsersUpdate**](CustodianProjectUsersApi.md#custodianProjectUsersUpdate) | **PUT** /api/v1/custodian_approvals/{custodianId}/projectUsers/{projectUserId} | Update custodian approval for a project user |


<a id="custodianProjectUsersIndex"></a>
# **custodianProjectUsersIndex**
> CustodianProjectUsersIndex200Response custodianProjectUsersIndex(custodianId)

List all project users associated with a custodian

Returns a list of all custodian project user approvals for a specific custodian

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.CustodianProjectUsersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CustodianProjectUsersApi apiInstance = new CustodianProjectUsersApi(defaultClient);
    Integer custodianId = 56; // Integer | ID of the custodian
    try {
      CustodianProjectUsersIndex200Response result = apiInstance.custodianProjectUsersIndex(custodianId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustodianProjectUsersApi#custodianProjectUsersIndex");
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
| **custodianId** | **Integer**| ID of the custodian | |

### Return type

[**CustodianProjectUsersIndex200Response**](CustodianProjectUsersIndex200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful operation |  -  |
| **400** | Invalid argument(s) |  -  |
| **403** | Forbidden |  -  |
| **404** | Custodian Not Found |  -  |

<a id="custodianProjectUsersShow"></a>
# **custodianProjectUsersShow**
> CustodianProjectUsersShow200Response custodianProjectUsersShow(custodianId, projectUserId)

Get custodian approval for a project user

Returns custodian approval details for a specific project user

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.CustodianProjectUsersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CustodianProjectUsersApi apiInstance = new CustodianProjectUsersApi(defaultClient);
    Integer custodianId = 56; // Integer | ID of the custodian
    Integer projectUserId = 56; // Integer | ID of the project user
    try {
      CustodianProjectUsersShow200Response result = apiInstance.custodianProjectUsersShow(custodianId, projectUserId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustodianProjectUsersApi#custodianProjectUsersShow");
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
| **custodianId** | **Integer**| ID of the custodian | |
| **projectUserId** | **Integer**| ID of the project user | |

### Return type

[**CustodianProjectUsersShow200Response**](CustodianProjectUsersShow200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful operation |  -  |
| **400** | Invalid argument(s) |  -  |
| **403** | Forbidden |  -  |
| **404** | Not Found |  -  |

<a id="custodianProjectUsersUpdate"></a>
# **custodianProjectUsersUpdate**
> CustodianProjectUsersShow200Response custodianProjectUsersUpdate(custodianId, projectUserId, custodianProjectUsersUpdateRequest)

Update custodian approval for a project user

Updates approval status and/or comment for a project user

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.CustodianProjectUsersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CustodianProjectUsersApi apiInstance = new CustodianProjectUsersApi(defaultClient);
    Integer custodianId = 56; // Integer | ID of the custodian
    Integer projectUserId = 56; // Integer | ID of the project user
    CustodianProjectUsersUpdateRequest custodianProjectUsersUpdateRequest = new CustodianProjectUsersUpdateRequest(); // CustodianProjectUsersUpdateRequest | 
    try {
      CustodianProjectUsersShow200Response result = apiInstance.custodianProjectUsersUpdate(custodianId, projectUserId, custodianProjectUsersUpdateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustodianProjectUsersApi#custodianProjectUsersUpdate");
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
| **custodianId** | **Integer**| ID of the custodian | |
| **projectUserId** | **Integer**| ID of the project user | |
| **custodianProjectUsersUpdateRequest** | [**CustodianProjectUsersUpdateRequest**](CustodianProjectUsersUpdateRequest.md)|  | |

### Return type

[**CustodianProjectUsersShow200Response**](CustodianProjectUsersShow200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful operation |  -  |
| **400** | Invalid argument(s) |  -  |
| **403** | Forbidden |  -  |
| **404** | Not Found |  -  |
| **500** | Bad Request |  -  |

