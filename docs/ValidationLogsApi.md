# ValidationLogsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**validationLogsGetCustodianOrganisationValidationLogs**](ValidationLogsApi.md#validationLogsGetCustodianOrganisationValidationLogs) | **GET** /api/v1/custodians/{custodianId}/organisation/{organisationId}/validation_logs | Get Validation Logs for Custodian and Organisation |
| [**validationLogsGetCustodianProjectUserValidationLogs**](ValidationLogsApi.md#validationLogsGetCustodianProjectUserValidationLogs) | **GET** /api/v1/custodians/{custodianId}/projects/{projectId}/registries/{registryId}/validation_logs | Get Validation Logs for Custodian, Project, and Registry |
| [**validationLogsUpdate**](ValidationLogsApi.md#validationLogsUpdate) | **PUT** /api/v1/validation_logs/{id} | Update a Validation Log |
| [**validationLogsUpdateCustodianValidationLogs**](ValidationLogsApi.md#validationLogsUpdateCustodianValidationLogs) | **PUT** /api/v1/custodians/{custodianId}/validation_Logs | Enable or Disable All Validation Logs for a Custodian Across Projects/Registries |


<a id="validationLogsGetCustodianOrganisationValidationLogs"></a>
# **validationLogsGetCustodianOrganisationValidationLogs**
> ValidationLogsGetCustodianProjectUserValidationLogs200Response validationLogsGetCustodianOrganisationValidationLogs(custodianId, organisationId, showDisabled)

Get Validation Logs for Custodian and Organisation

Retrieve validation logs associated with a given custodian and organisation.

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ValidationLogsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ValidationLogsApi apiInstance = new ValidationLogsApi(defaultClient);
    Integer custodianId = 56; // Integer | The ID of the custodian entity
    Integer organisationId = 56; // Integer | The ID of the organisation entity
    Boolean showDisabled = true; // Boolean | Whether to include disabled validation logs
    try {
      ValidationLogsGetCustodianProjectUserValidationLogs200Response result = apiInstance.validationLogsGetCustodianOrganisationValidationLogs(custodianId, organisationId, showDisabled);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ValidationLogsApi#validationLogsGetCustodianOrganisationValidationLogs");
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
| **custodianId** | **Integer**| The ID of the custodian entity | |
| **organisationId** | **Integer**| The ID of the organisation entity | |
| **showDisabled** | **Boolean**| Whether to include disabled validation logs | [optional] |

### Return type

[**ValidationLogsGetCustodianProjectUserValidationLogs200Response**](ValidationLogsGetCustodianProjectUserValidationLogs200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response with validation logs |  -  |
| **404** | Custodian or Organisation not found |  -  |
| **500** | Internal server error |  -  |

<a id="validationLogsGetCustodianProjectUserValidationLogs"></a>
# **validationLogsGetCustodianProjectUserValidationLogs**
> ValidationLogsGetCustodianProjectUserValidationLogs200Response validationLogsGetCustodianProjectUserValidationLogs(custodianId, projectId, registryId)

Get Validation Logs for Custodian, Project, and Registry

Retrieve validation logs associated with a given custodian, project, and registry.

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ValidationLogsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ValidationLogsApi apiInstance = new ValidationLogsApi(defaultClient);
    Integer custodianId = 56; // Integer | The ID of the custodian entity
    Integer projectId = 56; // Integer | The ID of the project entity
    Integer registryId = 56; // Integer | The ID of the registry entity
    try {
      ValidationLogsGetCustodianProjectUserValidationLogs200Response result = apiInstance.validationLogsGetCustodianProjectUserValidationLogs(custodianId, projectId, registryId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ValidationLogsApi#validationLogsGetCustodianProjectUserValidationLogs");
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
| **custodianId** | **Integer**| The ID of the custodian entity | |
| **projectId** | **Integer**| The ID of the project entity | |
| **registryId** | **Integer**| The ID of the registry entity | |

### Return type

[**ValidationLogsGetCustodianProjectUserValidationLogs200Response**](ValidationLogsGetCustodianProjectUserValidationLogs200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response with validation logs |  -  |

<a id="validationLogsUpdate"></a>
# **validationLogsUpdate**
> ValidationLogsUpdate200Response validationLogsUpdate(id, validationLogsUpdateRequest)

Update a Validation Log

Update a validation log entry, including marking it as complete, incomplete, passed, or failed.

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ValidationLogsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ValidationLogsApi apiInstance = new ValidationLogsApi(defaultClient);
    Integer id = 56; // Integer | The ID of the validation log entry
    ValidationLogsUpdateRequest validationLogsUpdateRequest = new ValidationLogsUpdateRequest(); // ValidationLogsUpdateRequest | 
    try {
      ValidationLogsUpdate200Response result = apiInstance.validationLogsUpdate(id, validationLogsUpdateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ValidationLogsApi#validationLogsUpdate");
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
| **id** | **Integer**| The ID of the validation log entry | |
| **validationLogsUpdateRequest** | [**ValidationLogsUpdateRequest**](ValidationLogsUpdateRequest.md)|  | [optional] |

### Return type

[**ValidationLogsUpdate200Response**](ValidationLogsUpdate200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Validation log status updated successfully |  -  |
| **404** | Validation log not found |  -  |

<a id="validationLogsUpdateCustodianValidationLogs"></a>
# **validationLogsUpdateCustodianValidationLogs**
> ValidationLogsUpdateCustodianValidationLogs200Response validationLogsUpdateCustodianValidationLogs(custodianId, validationLogsUpdateCustodianValidationLogsRequest)

Enable or Disable All Validation Logs for a Custodian Across Projects/Registries

Bulk update the enabled flag for all validation logs tied to a custodian and any project/registry.

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ValidationLogsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ValidationLogsApi apiInstance = new ValidationLogsApi(defaultClient);
    Integer custodianId = 56; // Integer | The ID of the custodian entity
    ValidationLogsUpdateCustodianValidationLogsRequest validationLogsUpdateCustodianValidationLogsRequest = new ValidationLogsUpdateCustodianValidationLogsRequest(); // ValidationLogsUpdateCustodianValidationLogsRequest | 
    try {
      ValidationLogsUpdateCustodianValidationLogs200Response result = apiInstance.validationLogsUpdateCustodianValidationLogs(custodianId, validationLogsUpdateCustodianValidationLogsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ValidationLogsApi#validationLogsUpdateCustodianValidationLogs");
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
| **custodianId** | **Integer**| The ID of the custodian entity | |
| **validationLogsUpdateCustodianValidationLogsRequest** | [**ValidationLogsUpdateCustodianValidationLogsRequest**](ValidationLogsUpdateCustodianValidationLogsRequest.md)|  | |

### Return type

[**ValidationLogsUpdateCustodianValidationLogs200Response**](ValidationLogsUpdateCustodianValidationLogs200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Validation logs updated successfully |  -  |
| **400** | Invalid request |  -  |

