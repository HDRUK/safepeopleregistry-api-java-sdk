# SubsidiariesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**subsidiariesDestroy**](SubsidiariesApi.md#subsidiariesDestroy) | **DELETE** /api/v1/subsidiaries/{subsidiaryId}/organisations/{organisationId} | subsidiaries@destroy |
| [**subsidiariesStore**](SubsidiariesApi.md#subsidiariesStore) | **POST** /api/v1/subsidiaries/organisations/{organisationId} | subsidiaries@store |
| [**subsidiariesUpdate**](SubsidiariesApi.md#subsidiariesUpdate) | **PUT** /api/v1/subsidiaries/{subsidiaryId}/organisations/{organisationId} | subsidiaries@update |


<a id="subsidiariesDestroy"></a>
# **subsidiariesDestroy**
> AffiliationDestroy200Response subsidiariesDestroy(organisationId, subsidiaryId)

subsidiaries@destroy

Delete an subsidiary entry from the system

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.SubsidiariesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    SubsidiariesApi apiInstance = new SubsidiariesApi(defaultClient);
    Integer organisationId = 1; // Integer | organisations entry ID
    Integer subsidiaryId = 1; // Integer | subsidiary entry ID
    try {
      AffiliationDestroy200Response result = apiInstance.subsidiariesDestroy(organisationId, subsidiaryId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SubsidiariesApi#subsidiariesDestroy");
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
| **organisationId** | **Integer**| organisations entry ID | |
| **subsidiaryId** | **Integer**| subsidiary entry ID | |

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

<a id="subsidiariesStore"></a>
# **subsidiariesStore**
> SubsidiariesStore201Response subsidiariesStore(organisationId, subsidiary)

subsidiaries@store

Create a subsidiary entry

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.SubsidiariesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    SubsidiariesApi apiInstance = new SubsidiariesApi(defaultClient);
    Integer organisationId = 1; // Integer | organisations entry ID
    Subsidiary subsidiary = new Subsidiary(); // Subsidiary | subsidiary definition
    try {
      SubsidiariesStore201Response result = apiInstance.subsidiariesStore(organisationId, subsidiary);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SubsidiariesApi#subsidiariesStore");
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
| **organisationId** | **Integer**| organisations entry ID | |
| **subsidiary** | [**Subsidiary**](Subsidiary.md)| subsidiary definition | |

### Return type

[**SubsidiariesStore201Response**](SubsidiariesStore201Response.md)

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
| **404** | Not found response |  -  |
| **500** | Error |  -  |

<a id="subsidiariesUpdate"></a>
# **subsidiariesUpdate**
> SubsidiariesStore201Response subsidiariesUpdate(organisationId, subsidiaryId, subsidiary)

subsidiaries@update

Update a subsidiary entry

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.SubsidiariesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    SubsidiariesApi apiInstance = new SubsidiariesApi(defaultClient);
    Integer organisationId = 1; // Integer | organisations entry ID
    Integer subsidiaryId = 1; // Integer | subsidiary entry ID
    Subsidiary subsidiary = new Subsidiary(); // Subsidiary | subsidiary definition
    try {
      SubsidiariesStore201Response result = apiInstance.subsidiariesUpdate(organisationId, subsidiaryId, subsidiary);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SubsidiariesApi#subsidiariesUpdate");
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
| **organisationId** | **Integer**| organisations entry ID | |
| **subsidiaryId** | **Integer**| subsidiary entry ID | |
| **subsidiary** | [**Subsidiary**](Subsidiary.md)| subsidiary definition | |

### Return type

[**SubsidiariesStore201Response**](SubsidiariesStore201Response.md)

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

