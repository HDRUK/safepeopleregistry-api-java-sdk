# OrganisationApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**organisationGetDelegates**](OrganisationApi.md#organisationGetDelegates) | **GET** /api/v1/organisations/{id}/delegates | Return all delegates associated with an organisation |
| [**organisationGetProjects**](OrganisationApi.md#organisationGetProjects) | **GET** /api/v1/organisations/{id}/projects | organisation@getProjects |
| [**organisationGetSponsorshipsProjects**](OrganisationApi.md#organisationGetSponsorshipsProjects) | **GET** /api/v1/organisations/{id}/projects/sponsorships | organisation@getSponsorshipsProjects |
| [**organisationGetUsers**](OrganisationApi.md#organisationGetUsers) | **GET** /api/v1/organisations/{id}/users | organisation@getUsers |
| [**organisationIndex**](OrganisationApi.md#organisationIndex) | **GET** /api/v1/organisations | organisation@index |


<a id="organisationGetDelegates"></a>
# **organisationGetDelegates**
> OrganisationGetDelegates200Response organisationGetDelegates(id)

Return all delegates associated with an organisation

Return all delegates associated with an organisation

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.OrganisationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    OrganisationApi apiInstance = new OrganisationApi(defaultClient);
    Integer id = 1; // Integer | Organisation ID
    try {
      OrganisationGetDelegates200Response result = apiInstance.organisationGetDelegates(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrganisationApi#organisationGetDelegates");
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

[**OrganisationGetDelegates200Response**](OrganisationGetDelegates200Response.md)

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

<a id="organisationGetProjects"></a>
# **organisationGetProjects**
> OrganisationGetProjects200Response organisationGetProjects(id)

organisation@getProjects

Return an all projects associated with an organisation (i.e. data-custodian)

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.OrganisationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    OrganisationApi apiInstance = new OrganisationApi(defaultClient);
    Integer id = 1; // Integer | Organisation ID
    try {
      OrganisationGetProjects200Response result = apiInstance.organisationGetProjects(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrganisationApi#organisationGetProjects");
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

[**OrganisationGetProjects200Response**](OrganisationGetProjects200Response.md)

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

<a id="organisationGetSponsorshipsProjects"></a>
# **organisationGetSponsorshipsProjects**
> OrganisationGetProjects200Response organisationGetSponsorshipsProjects(id)

organisation@getSponsorshipsProjects

Return an all projects associated with an organisation with sponsorships (i.e. data-custodian)

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.OrganisationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    OrganisationApi apiInstance = new OrganisationApi(defaultClient);
    Integer id = 1; // Integer | Organisation ID
    try {
      OrganisationGetProjects200Response result = apiInstance.organisationGetSponsorshipsProjects(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrganisationApi#organisationGetSponsorshipsProjects");
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

[**OrganisationGetProjects200Response**](OrganisationGetProjects200Response.md)

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

<a id="organisationGetUsers"></a>
# **organisationGetUsers**
> OrganisationGetUsers200Response organisationGetUsers(id)

organisation@getUsers

Return all users associated with an organisation

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.OrganisationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    OrganisationApi apiInstance = new OrganisationApi(defaultClient);
    Integer id = 1; // Integer | Organisation ID
    try {
      OrganisationGetUsers200Response result = apiInstance.organisationGetUsers(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrganisationApi#organisationGetUsers");
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

[**OrganisationGetUsers200Response**](OrganisationGetUsers200Response.md)

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

<a id="organisationIndex"></a>
# **organisationIndex**
> OrganisationIndex200Response organisationIndex()

organisation@index

Return a list of organisations

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.OrganisationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    OrganisationApi apiInstance = new OrganisationApi(defaultClient);
    try {
      OrganisationIndex200Response result = apiInstance.organisationIndex();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrganisationApi#organisationIndex");
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
| **404** | Not found response |  -  |

