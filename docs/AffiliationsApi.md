# AffiliationsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**affiliationsGetOrganisationAffiliation**](AffiliationsApi.md#affiliationsGetOrganisationAffiliation) | **GET** /api/v1/affiliations/{registryId}/organisation/{organisationId} | Return a specific organisation&#39;s affiliation by registry ID and organisation ID |
| [**affiliationsIndexByRegistryId**](AffiliationsApi.md#affiliationsIndexByRegistryId) | **GET** /api/v1/affiliations/{registryId} | Affiliations@show |
| [**affiliationsStoreByRegistryId**](AffiliationsApi.md#affiliationsStoreByRegistryId) | **POST** /api/v1/affiliations/{registryId} | Affiliations@store |
| [**affiliationsUpdate**](AffiliationsApi.md#affiliationsUpdate) | **PUT** /api/v1/affiliations/{id} | Affiliations@update |
| [**affiliationsVerifyEmail**](AffiliationsApi.md#affiliationsVerifyEmail) | **PUT** /api/v1/affiliations/verify_email/{verificationCode} | Affiliations@verifyEmail |


<a id="affiliationsGetOrganisationAffiliation"></a>
# **affiliationsGetOrganisationAffiliation**
> AffiliationsGetOrganisationAffiliation200Response affiliationsGetOrganisationAffiliation(registryId, organisationId)

Return a specific organisation&#39;s affiliation by registry ID and organisation ID

Get a specific organisation&#39;s affiliation for a given registry

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.AffiliationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    AffiliationsApi apiInstance = new AffiliationsApi(defaultClient);
    Integer registryId = 1; // Integer | Registry ID
    Integer organisationId = 100; // Integer | Organisation ID
    try {
      AffiliationsGetOrganisationAffiliation200Response result = apiInstance.affiliationsGetOrganisationAffiliation(registryId, organisationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AffiliationsApi#affiliationsGetOrganisationAffiliation");
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
| **registryId** | **Integer**| Registry ID | |
| **organisationId** | **Integer**| Organisation ID | |

### Return type

[**AffiliationsGetOrganisationAffiliation200Response**](AffiliationsGetOrganisationAffiliation200Response.md)

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
| **404** | Affiliation not found |  -  |

<a id="affiliationsIndexByRegistryId"></a>
# **affiliationsIndexByRegistryId**
> AffiliationsIndexByRegistryId200Response affiliationsIndexByRegistryId(registryId)

Affiliations@show

Return a list of affiliations by registry id

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.AffiliationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    AffiliationsApi apiInstance = new AffiliationsApi(defaultClient);
    Integer registryId = 1; // Integer | Affiliations registry id
    try {
      AffiliationsIndexByRegistryId200Response result = apiInstance.affiliationsIndexByRegistryId(registryId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AffiliationsApi#affiliationsIndexByRegistryId");
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
| **registryId** | **Integer**| Affiliations registry id | |

### Return type

[**AffiliationsIndexByRegistryId200Response**](AffiliationsIndexByRegistryId200Response.md)

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

<a id="affiliationsStoreByRegistryId"></a>
# **affiliationsStoreByRegistryId**
> AffiliationsStoreByRegistryId200Response affiliationsStoreByRegistryId(registryId, affiliation)

Affiliations@store

Create an Affiliation entry

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.AffiliationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    AffiliationsApi apiInstance = new AffiliationsApi(defaultClient);
    Integer registryId = 1; // Integer | Registry entry ID
    Affiliation affiliation = new Affiliation(); // Affiliation | Affiliation definition
    try {
      AffiliationsStoreByRegistryId200Response result = apiInstance.affiliationsStoreByRegistryId(registryId, affiliation);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AffiliationsApi#affiliationsStoreByRegistryId");
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
| **registryId** | **Integer**| Registry entry ID | |
| **affiliation** | [**Affiliation**](Affiliation.md)| Affiliation definition | |

### Return type

[**AffiliationsStoreByRegistryId200Response**](AffiliationsStoreByRegistryId200Response.md)

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

<a id="affiliationsUpdate"></a>
# **affiliationsUpdate**
> AffiliationsStoreByRegistryId200Response affiliationsUpdate(id, affiliation)

Affiliations@update

Update an Affiliation entry

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.AffiliationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    AffiliationsApi apiInstance = new AffiliationsApi(defaultClient);
    Integer id = 1; // Integer | Affiliation entry ID
    Affiliation affiliation = new Affiliation(); // Affiliation | Affiliation definition
    try {
      AffiliationsStoreByRegistryId200Response result = apiInstance.affiliationsUpdate(id, affiliation);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AffiliationsApi#affiliationsUpdate");
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
| **id** | **Integer**| Affiliation entry ID | |
| **affiliation** | [**Affiliation**](Affiliation.md)| Affiliation definition | |

### Return type

[**AffiliationsStoreByRegistryId200Response**](AffiliationsStoreByRegistryId200Response.md)

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

<a id="affiliationsVerifyEmail"></a>
# **affiliationsVerifyEmail**
> AffiliationsStoreByRegistryId200Response affiliationsVerifyEmail(verificationCode)

Affiliations@verifyEmail

Update an Affiliation entry with verification

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.AffiliationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    AffiliationsApi apiInstance = new AffiliationsApi(defaultClient);
    String verificationCode = "1"; // String | Email verification code
    try {
      AffiliationsStoreByRegistryId200Response result = apiInstance.affiliationsVerifyEmail(verificationCode);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AffiliationsApi#affiliationsVerifyEmail");
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
| **verificationCode** | **String**| Email verification code | |

### Return type

[**AffiliationsStoreByRegistryId200Response**](AffiliationsStoreByRegistryId200Response.md)

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

