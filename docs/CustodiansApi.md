# CustodiansApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**custodiansCreateCustodianValidationChecks**](CustodiansApi.md#custodiansCreateCustodianValidationChecks) | **POST** /api/v1/custodians/{custodianId}/validation_checks | Assign a validation check to a custodian |
| [**custodiansGetCustodianUsers**](CustodiansApi.md#custodiansGetCustodianUsers) | **GET** /api/v1/custodians/{custodianId}/custodian_users | Get list of people for a custodian |
| [**custodiansGetCustodianValidationChecks**](CustodiansApi.md#custodiansGetCustodianValidationChecks) | **GET** /api/v1/custodians/{custodianId}/validation_checks | Get validation checks assigned to a custodian |
| [**custodiansGetOrganisationUsers**](CustodiansApi.md#custodiansGetOrganisationUsers) | **GET** /api/v1/custodians/{custodianId}/organisations/{organisationId}/users | Get list of people for organisation |
| [**custodiansGetRules**](CustodiansApi.md#custodiansGetRules) | **GET** /api/v1/custodians/{id}/rules | Get rules for a specific custodian |
| [**custodiansGetStatusesUsers**](CustodiansApi.md#custodiansGetStatusesUsers) | **GET** /api/v1/custodians/{custodianId}/projectUsers/{projectUserId}/statuses | Get statuses for a user in a project/organisation/custodian |


<a id="custodiansCreateCustodianValidationChecks"></a>
# **custodiansCreateCustodianValidationChecks**
> ValidationCheck custodiansCreateCustodianValidationChecks(custodianId, custodiansCreateCustodianValidationChecksRequest)

Assign a validation check to a custodian

Creates a new validation check and assigns it to a specific custodian via the custodian_has_validation_check pivot table.

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.CustodiansApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CustodiansApi apiInstance = new CustodiansApi(defaultClient);
    Integer custodianId = 56; // Integer | ID of the custodian
    CustodiansCreateCustodianValidationChecksRequest custodiansCreateCustodianValidationChecksRequest = new CustodiansCreateCustodianValidationChecksRequest(); // CustodiansCreateCustodianValidationChecksRequest | 
    try {
      ValidationCheck result = apiInstance.custodiansCreateCustodianValidationChecks(custodianId, custodiansCreateCustodianValidationChecksRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustodiansApi#custodiansCreateCustodianValidationChecks");
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
| **custodiansCreateCustodianValidationChecksRequest** | [**CustodiansCreateCustodianValidationChecksRequest**](CustodiansCreateCustodianValidationChecksRequest.md)|  | |

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
| **201** | Validation check created and assigned successfully |  -  |
| **400** | Invalid input |  -  |
| **404** | Custodian not found |  -  |

<a id="custodiansGetCustodianUsers"></a>
# **custodiansGetCustodianUsers**
> CustodiansGetCustodianUsers200Response custodiansGetCustodianUsers(custodianId)

Get list of people for a custodian

Fetches the list of custodian users based on the custodian id.

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.CustodiansApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CustodiansApi apiInstance = new CustodiansApi(defaultClient);
    Integer custodianId = 56; // Integer | ID of the custodian
    try {
      CustodiansGetCustodianUsers200Response result = apiInstance.custodiansGetCustodianUsers(custodianId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustodiansApi#custodiansGetCustodianUsers");
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

[**CustodiansGetCustodianUsers200Response**](CustodiansGetCustodianUsers200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved custodian users |  -  |
| **400** | Invalid argument(s) |  -  |
| **404** | Custodian users not found |  -  |

<a id="custodiansGetCustodianValidationChecks"></a>
# **custodiansGetCustodianValidationChecks**
> List&lt;ValidationCheck&gt; custodiansGetCustodianValidationChecks(custodianId)

Get validation checks assigned to a custodian

Returns the list of validation checks associated with a specific custodian.

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.CustodiansApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CustodiansApi apiInstance = new CustodiansApi(defaultClient);
    Integer custodianId = 56; // Integer | ID of the custodian
    try {
      List<ValidationCheck> result = apiInstance.custodiansGetCustodianValidationChecks(custodianId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustodiansApi#custodiansGetCustodianValidationChecks");
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
| **400** | Invalid argument(s) |  -  |
| **404** | Custodian not found |  -  |

<a id="custodiansGetOrganisationUsers"></a>
# **custodiansGetOrganisationUsers**
> CustodiansGetOrganisationUsers200Response custodiansGetOrganisationUsers(custodianId, organisationId)

Get list of people for organisation

Fetches the list of users associated with the given custodian and organisations IDs.

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.CustodiansApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CustodiansApi apiInstance = new CustodiansApi(defaultClient);
    Integer custodianId = 56; // Integer | ID of the custodian
    Integer organisationId = 56; // Integer | ID of the organisation
    try {
      CustodiansGetOrganisationUsers200Response result = apiInstance.custodiansGetOrganisationUsers(custodianId, organisationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustodiansApi#custodiansGetOrganisationUsers");
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
| **organisationId** | **Integer**| ID of the organisation | |

### Return type

[**CustodiansGetOrganisationUsers200Response**](CustodiansGetOrganisationUsers200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved organisation users |  -  |
| **400** | Invalid argument(s) |  -  |
| **404** | Organisation users not found |  -  |

<a id="custodiansGetRules"></a>
# **custodiansGetRules**
> CustodiansGetRules200Response custodiansGetRules(id)

Get rules for a specific custodian

Fetches the list of rules associated with the given custodian ID.

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.CustodiansApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CustodiansApi apiInstance = new CustodiansApi(defaultClient);
    Integer id = 56; // Integer | ID of the custodian
    try {
      CustodiansGetRules200Response result = apiInstance.custodiansGetRules(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustodiansApi#custodiansGetRules");
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
| **id** | **Integer**| ID of the custodian | |

### Return type

[**CustodiansGetRules200Response**](CustodiansGetRules200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved rules |  -  |
| **400** | Invalid argument(s) |  -  |
| **404** | Custodian not found |  -  |

<a id="custodiansGetStatusesUsers"></a>
# **custodiansGetStatusesUsers**
> CustodiansGetOrganisationUsers200Response custodiansGetStatusesUsers(custodianId, projectUserId)

Get statuses for a user in a project/organisation/custodian

Fetches the user statuses given custodian and organisations and project and user IDs.

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.CustodiansApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CustodiansApi apiInstance = new CustodiansApi(defaultClient);
    Integer custodianId = 56; // Integer | ID of the custodian
    Integer projectUserId = 56; // Integer | ID of the project user
    try {
      CustodiansGetOrganisationUsers200Response result = apiInstance.custodiansGetStatusesUsers(custodianId, projectUserId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustodiansApi#custodiansGetStatusesUsers");
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

[**CustodiansGetOrganisationUsers200Response**](CustodiansGetOrganisationUsers200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved organisation users |  -  |
| **400** | Invalid argument(s) |  -  |
| **404** | Organisation users not found |  -  |

