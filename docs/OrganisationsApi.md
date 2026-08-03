# OrganisationsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**custodianProjectOrganisationsGetStatus**](OrganisationsApi.md#custodianProjectOrganisationsGetStatus) | **GET** /api/v1/custodian_approvals/{custodianId}/project/{projectId}/organisation/{organisationId}/projectOrganisations/status | Get project organisation status |
| [**organisationsCustodianInviteUser**](OrganisationsApi.md#organisationsCustodianInviteUser) | **POST** /api/v1/organisations/{id}/custodian_invite_user | organisations@custodian_invite_user |
| [**organisationsDestroy**](OrganisationsApi.md#organisationsDestroy) | **DELETE** /api/v1/organisations/{id} | organisations@destroy |
| [**organisationsGetRegistries**](OrganisationsApi.md#organisationsGetRegistries) | **GET** /api/v1/organisations/{id}/registries | Get all registries for an organisation |
| [**organisationsGetStatus**](OrganisationsApi.md#organisationsGetStatus) | **GET** /api/v1/organisations/{id}/status | Get organisation status |
| [**organisationsIdvt**](OrganisationsApi.md#organisationsIdvt) | **GET** /api/v1/organisations/{id}/idvt | organisations@idvt |
| [**organisationsInviteUser**](OrganisationsApi.md#organisationsInviteUser) | **POST** /api/v1/organisations/{id}/invite_user | organisations@invite_user |
| [**organisationsShow**](OrganisationsApi.md#organisationsShow) | **GET** /api/v1/organisations/{id} | organisations@show |
| [**organisationsStore**](OrganisationsApi.md#organisationsStore) | **POST** /api/v1/organisations | organisations@store |
| [**organisationsUpdate**](OrganisationsApi.md#organisationsUpdate) | **PUT** /api/v1/organisations/{id} | organisations@update |
| [**organisationsUpdateApproved**](OrganisationsApi.md#organisationsUpdateApproved) | **PUT** /api/v1/organisations/{id}/approved | SuperAdmin update org system_approved flag |


<a id="custodianProjectOrganisationsGetStatus"></a>
# **custodianProjectOrganisationsGetStatus**
> CustodianProjectOrganisationsGetStatus200Response custodianProjectOrganisationsGetStatus(custodianId, projectId, organisationId)

Get project organisation status

Retrieve the status of a project organisation for a specific custodian using custodianId, projectId, and organisationId.

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.OrganisationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    OrganisationsApi apiInstance = new OrganisationsApi(defaultClient);
    Integer custodianId = 1; // Integer | Custodian ID
    Integer projectId = 10; // Integer | Project ID
    Integer organisationId = 5; // Integer | Organisation ID
    try {
      CustodianProjectOrganisationsGetStatus200Response result = apiInstance.custodianProjectOrganisationsGetStatus(custodianId, projectId, organisationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrganisationsApi#custodianProjectOrganisationsGetStatus");
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
| **custodianId** | **Integer**| Custodian ID | |
| **projectId** | **Integer**| Project ID | |
| **organisationId** | **Integer**| Organisation ID | |

### Return type

[**CustodianProjectOrganisationsGetStatus200Response**](CustodianProjectOrganisationsGetStatus200Response.md)

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
| **404** | Organisation or custodian project organisation not found |  -  |
| **500** | Server error |  -  |

<a id="organisationsCustodianInviteUser"></a>
# **organisationsCustodianInviteUser**
> AccreditationStoreByRegistryId201Response organisationsCustodianInviteUser(id, organisationsInviteUserRequest)

organisations@custodian_invite_user

Invites a user to org

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.OrganisationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    OrganisationsApi apiInstance = new OrganisationsApi(defaultClient);
    Integer id = 1; // Integer | organisations entry ID
    OrganisationsInviteUserRequest organisationsInviteUserRequest = new OrganisationsInviteUserRequest(); // OrganisationsInviteUserRequest | Invite definition
    try {
      AccreditationStoreByRegistryId201Response result = apiInstance.organisationsCustodianInviteUser(id, organisationsInviteUserRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrganisationsApi#organisationsCustodianInviteUser");
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
| **id** | **Integer**| organisations entry ID | |
| **organisationsInviteUserRequest** | [**OrganisationsInviteUserRequest**](OrganisationsInviteUserRequest.md)| Invite definition | |

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
| **201** | Success |  -  |
| **400** | Invalid argument(s) |  -  |
| **500** | Error |  -  |

<a id="organisationsDestroy"></a>
# **organisationsDestroy**
> AffiliationDestroy200Response organisationsDestroy(id)

organisations@destroy

Delete an organisations entry from the system

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.OrganisationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    OrganisationsApi apiInstance = new OrganisationsApi(defaultClient);
    Integer id = 1; // Integer | organisations entry ID
    try {
      AffiliationDestroy200Response result = apiInstance.organisationsDestroy(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrganisationsApi#organisationsDestroy");
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
| **id** | **Integer**| organisations entry ID | |

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

<a id="organisationsGetRegistries"></a>
# **organisationsGetRegistries**
> OrganisationsGetRegistries200Response organisationsGetRegistries(id, showPending)

Get all registries for an organisation

Returns all registries associated with the specified organisation

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.OrganisationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    OrganisationsApi apiInstance = new OrganisationsApi(defaultClient);
    Long id = 56L; // Long | Organisation ID
    Boolean showPending = true; // Boolean | Include users with pending invitations (true/false)
    try {
      OrganisationsGetRegistries200Response result = apiInstance.organisationsGetRegistries(id, showPending);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrganisationsApi#organisationsGetRegistries");
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
| **id** | **Long**| Organisation ID | |
| **showPending** | **Boolean**| Include users with pending invitations (true/false) | [optional] |

### Return type

[**OrganisationsGetRegistries200Response**](OrganisationsGetRegistries200Response.md)

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
| **404** | No registries found for this organisation |  -  |

<a id="organisationsGetStatus"></a>
# **organisationsGetStatus**
> CustodianProjectOrganisationsGetStatus200Response organisationsGetStatus(id)

Get organisation status

Returns the organisation with its model state and state

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.OrganisationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    OrganisationsApi apiInstance = new OrganisationsApi(defaultClient);
    Integer id = 1; // Integer | Organisation ID
    try {
      CustodianProjectOrganisationsGetStatus200Response result = apiInstance.organisationsGetStatus(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrganisationsApi#organisationsGetStatus");
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
| **id** | **Integer**| Organisation ID | |

### Return type

[**CustodianProjectOrganisationsGetStatus200Response**](CustodianProjectOrganisationsGetStatus200Response.md)

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
| **404** | Organisation not found |  -  |

<a id="organisationsIdvt"></a>
# **organisationsIdvt**
> OrganisationsIdvt200Response organisationsIdvt(id)

organisations@idvt

Return an organisations idvt details by ID

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.OrganisationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    OrganisationsApi apiInstance = new OrganisationsApi(defaultClient);
    Integer id = 1; // Integer | organisations entry ID
    try {
      OrganisationsIdvt200Response result = apiInstance.organisationsIdvt(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrganisationsApi#organisationsIdvt");
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
| **id** | **Integer**| organisations entry ID | |

### Return type

[**OrganisationsIdvt200Response**](OrganisationsIdvt200Response.md)

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

<a id="organisationsInviteUser"></a>
# **organisationsInviteUser**
> AccreditationStoreByRegistryId201Response organisationsInviteUser(id, organisationsInviteUserRequest)

organisations@invite_user

Invites a user to org

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.OrganisationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    OrganisationsApi apiInstance = new OrganisationsApi(defaultClient);
    Integer id = 1; // Integer | organisations entry ID
    OrganisationsInviteUserRequest organisationsInviteUserRequest = new OrganisationsInviteUserRequest(); // OrganisationsInviteUserRequest | Invite definition
    try {
      AccreditationStoreByRegistryId201Response result = apiInstance.organisationsInviteUser(id, organisationsInviteUserRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrganisationsApi#organisationsInviteUser");
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
| **id** | **Integer**| organisations entry ID | |
| **organisationsInviteUserRequest** | [**OrganisationsInviteUserRequest**](OrganisationsInviteUserRequest.md)| Invite definition | |

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
| **201** | Success |  -  |
| **400** | Invalid argument(s) |  -  |
| **403** | forbidden |  -  |
| **500** | Error |  -  |

<a id="organisationsShow"></a>
# **organisationsShow**
> OrganisationIndex200Response organisationsShow(id)

organisations@show

Return an organisations entry by ID

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.OrganisationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    OrganisationsApi apiInstance = new OrganisationsApi(defaultClient);
    Integer id = 1; // Integer | organisations entry ID
    try {
      OrganisationIndex200Response result = apiInstance.organisationsShow(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrganisationsApi#organisationsShow");
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
| **id** | **Integer**| organisations entry ID | |

### Return type

[**OrganisationIndex200Response**](OrganisationIndex200Response.md)

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

<a id="organisationsStore"></a>
# **organisationsStore**
> IdentityStore201Response organisationsStore(organisation)

organisations@store

Create a organisations entry

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.OrganisationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    OrganisationsApi apiInstance = new OrganisationsApi(defaultClient);
    Organisation organisation = new Organisation(); // Organisation | organisations definition
    try {
      IdentityStore201Response result = apiInstance.organisationsStore(organisation);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrganisationsApi#organisationsStore");
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
| **organisation** | [**Organisation**](Organisation.md)| organisations definition | |

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
| **404** | Not found response |  -  |
| **201** | Success |  -  |
| **500** | Error |  -  |

<a id="organisationsUpdate"></a>
# **organisationsUpdate**
> OrganisationsUpdate200Response organisationsUpdate(id, organisation)

organisations@update

Update a organisations entry

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.OrganisationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    OrganisationsApi apiInstance = new OrganisationsApi(defaultClient);
    Integer id = 1; // Integer | organisations entry ID
    Organisation organisation = new Organisation(); // Organisation | organisations definition
    try {
      OrganisationsUpdate200Response result = apiInstance.organisationsUpdate(id, organisation);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrganisationsApi#organisationsUpdate");
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
| **id** | **Integer**| organisations entry ID | |
| **organisation** | [**Organisation**](Organisation.md)| organisations definition | |

### Return type

[**OrganisationsUpdate200Response**](OrganisationsUpdate200Response.md)

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

<a id="organisationsUpdateApproved"></a>
# **organisationsUpdateApproved**
> AccreditationStoreByRegistryId201Response organisationsUpdateApproved(id, organisationsUpdateApprovedRequest)

SuperAdmin update org system_approved flag

Updates the system_approved flag for an organisation

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.OrganisationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    OrganisationsApi apiInstance = new OrganisationsApi(defaultClient);
    Integer id = 1; // Integer | organisations entry ID
    OrganisationsUpdateApprovedRequest organisationsUpdateApprovedRequest = new OrganisationsUpdateApprovedRequest(); // OrganisationsUpdateApprovedRequest | System approval update definition
    try {
      AccreditationStoreByRegistryId201Response result = apiInstance.organisationsUpdateApproved(id, organisationsUpdateApprovedRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrganisationsApi#organisationsUpdateApproved");
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
| **id** | **Integer**| organisations entry ID | |
| **organisationsUpdateApprovedRequest** | [**OrganisationsUpdateApprovedRequest**](OrganisationsUpdateApprovedRequest.md)| System approval update definition | |

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
| **201** | Success |  -  |
| **400** | Invalid argument(s) |  -  |
| **500** | Error |  -  |

