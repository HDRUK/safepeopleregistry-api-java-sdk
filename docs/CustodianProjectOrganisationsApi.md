# CustodianProjectOrganisationsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**custodianProjectOrganisationsGetWorkflowStates**](CustodianProjectOrganisationsApi.md#custodianProjectOrganisationsGetWorkflowStates) | **GET** /api/v1/custodian_approvals/projectOrganisations/getWorkflowStates | Get all workflow states for custodian project organisation approvals |
| [**custodianProjectOrganisationsIndex**](CustodianProjectOrganisationsApi.md#custodianProjectOrganisationsIndex) | **GET** /api/v1/custodian_approvals/{custodianId}/projectOrganisations | List all project organisations associated with a custodian |
| [**custodianProjectOrganisationsShow**](CustodianProjectOrganisationsApi.md#custodianProjectOrganisationsShow) | **GET** /api/v1/custodian_approvals/{custodianId}/projectOrganisations/{projectOrganisationId} | Get custodian approval for a project organisation |
| [**custodianProjectOrganisationsUpdate**](CustodianProjectOrganisationsApi.md#custodianProjectOrganisationsUpdate) | **PUT** /api/v1/custodian_approvals/{custodianId}/projectOrganisations/{projectOrganisationId} | Update custodian approval for a project organisation |


<a id="custodianProjectOrganisationsGetWorkflowStates"></a>
# **custodianProjectOrganisationsGetWorkflowStates**
> CustodianProjectOrganisationsGetWorkflowStates200Response custodianProjectOrganisationsGetWorkflowStates()

Get all workflow states for custodian project organisation approvals

Returns a list of all possible workflow states

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.CustodianProjectOrganisationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CustodianProjectOrganisationsApi apiInstance = new CustodianProjectOrganisationsApi(defaultClient);
    try {
      CustodianProjectOrganisationsGetWorkflowStates200Response result = apiInstance.custodianProjectOrganisationsGetWorkflowStates();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustodianProjectOrganisationsApi#custodianProjectOrganisationsGetWorkflowStates");
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

[**CustodianProjectOrganisationsGetWorkflowStates200Response**](CustodianProjectOrganisationsGetWorkflowStates200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful operation |  -  |

<a id="custodianProjectOrganisationsIndex"></a>
# **custodianProjectOrganisationsIndex**
> CustodianProjectOrganisationsIndex200Response custodianProjectOrganisationsIndex(custodianId)

List all project organisations associated with a custodian

Returns a list of all custodian project organisation approvals for a specific custodian

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.CustodianProjectOrganisationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CustodianProjectOrganisationsApi apiInstance = new CustodianProjectOrganisationsApi(defaultClient);
    Integer custodianId = 56; // Integer | ID of the custodian
    try {
      CustodianProjectOrganisationsIndex200Response result = apiInstance.custodianProjectOrganisationsIndex(custodianId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustodianProjectOrganisationsApi#custodianProjectOrganisationsIndex");
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

[**CustodianProjectOrganisationsIndex200Response**](CustodianProjectOrganisationsIndex200Response.md)

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

<a id="custodianProjectOrganisationsShow"></a>
# **custodianProjectOrganisationsShow**
> CustodianProjectOrganisationsShow200Response custodianProjectOrganisationsShow(custodianId, projectOrganisationId)

Get custodian approval for a project organisation

Returns custodian approval details for a specific project organisation

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.CustodianProjectOrganisationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CustodianProjectOrganisationsApi apiInstance = new CustodianProjectOrganisationsApi(defaultClient);
    Integer custodianId = 56; // Integer | ID of the custodian
    Integer projectOrganisationId = 56; // Integer | ID of the project organisation
    try {
      CustodianProjectOrganisationsShow200Response result = apiInstance.custodianProjectOrganisationsShow(custodianId, projectOrganisationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustodianProjectOrganisationsApi#custodianProjectOrganisationsShow");
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
| **projectOrganisationId** | **Integer**| ID of the project organisation | |

### Return type

[**CustodianProjectOrganisationsShow200Response**](CustodianProjectOrganisationsShow200Response.md)

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

<a id="custodianProjectOrganisationsUpdate"></a>
# **custodianProjectOrganisationsUpdate**
> CustodianProjectOrganisationsShow200Response custodianProjectOrganisationsUpdate(custodianId, projectOrganisationId, custodianProjectOrganisationsUpdateRequest)

Update custodian approval for a project organisation

Updates approval status and/or comment for a project organisation

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.CustodianProjectOrganisationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CustodianProjectOrganisationsApi apiInstance = new CustodianProjectOrganisationsApi(defaultClient);
    Integer custodianId = 56; // Integer | ID of the custodian
    Integer projectOrganisationId = 56; // Integer | ID of the project organisation
    CustodianProjectOrganisationsUpdateRequest custodianProjectOrganisationsUpdateRequest = new CustodianProjectOrganisationsUpdateRequest(); // CustodianProjectOrganisationsUpdateRequest | 
    try {
      CustodianProjectOrganisationsShow200Response result = apiInstance.custodianProjectOrganisationsUpdate(custodianId, projectOrganisationId, custodianProjectOrganisationsUpdateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustodianProjectOrganisationsApi#custodianProjectOrganisationsUpdate");
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
| **projectOrganisationId** | **Integer**| ID of the project organisation | |
| **custodianProjectOrganisationsUpdateRequest** | [**CustodianProjectOrganisationsUpdateRequest**](CustodianProjectOrganisationsUpdateRequest.md)|  | |

### Return type

[**CustodianProjectOrganisationsShow200Response**](CustodianProjectOrganisationsShow200Response.md)

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

