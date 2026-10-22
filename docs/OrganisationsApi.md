# OrganisationsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**organisationsAppointSro**](OrganisationsApi.md#organisationsAppointSro) | **PUT** /api/v1/organisations/{id}/sro | organisations@appointSro |
| [**organisationsInviteSro**](OrganisationsApi.md#organisationsInviteSro) | **POST** /api/v1/organisations/{id}/sro/invite | organisations@inviteSro |
| [**organisationsRemoveDelegate**](OrganisationsApi.md#organisationsRemoveDelegate) | **DELETE** /api/v1/organisations/{id}/delegates/{userId} | organisations@removeDelegate |
| [**organisationsResendSroInvite**](OrganisationsApi.md#organisationsResendSroInvite) | **POST** /api/v1/organisations/{id}/sro/resend_invite | organisations@resendSroInvite |


<a id="organisationsAppointSro"></a>
# **organisationsAppointSro**
> OrganisationsAppointSro200Response organisationsAppointSro(id, organisationsAppointSroRequest)

organisations@appointSro

Hands the SRO role over immediately: the appointee becomes SRO, the current SRO becomes a delegate, and an invited SRO keeps their invitation but will join as a delegate. Delegates can appoint while the organisation has no claimed SRO; after that only the SRO can.

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
    OrganisationsAppointSroRequest organisationsAppointSroRequest = new OrganisationsAppointSroRequest(); // OrganisationsAppointSroRequest | 
    try {
      OrganisationsAppointSro200Response result = apiInstance.organisationsAppointSro(id, organisationsAppointSroRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrganisationsApi#organisationsAppointSro");
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
| **organisationsAppointSroRequest** | [**OrganisationsAppointSroRequest**](OrganisationsAppointSroRequest.md)|  | |

### Return type

[**OrganisationsAppointSro200Response**](OrganisationsAppointSro200Response.md)

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
| **403** | Forbidden |  -  |
| **404** | The user is not a claimed member of this organisation |  -  |

<a id="organisationsInviteSro"></a>
# **organisationsInviteSro**
> OrganisationsInviteSro201Response organisationsInviteSro(id, organisationsInviteSroRequest)

organisations@inviteSro

Creates an invited (unclaimed) SRO and emails them an invitation. The current SRO keeps the role until the invitee claims their account; any other invited SRO keeps their invitation but will join as a delegate. Delegates can invite while the organisation has no claimed SRO; after that only the SRO can.

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
    OrganisationsInviteSroRequest organisationsInviteSroRequest = new OrganisationsInviteSroRequest(); // OrganisationsInviteSroRequest | 
    try {
      OrganisationsInviteSro201Response result = apiInstance.organisationsInviteSro(id, organisationsInviteSroRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrganisationsApi#organisationsInviteSro");
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
| **organisationsInviteSroRequest** | [**OrganisationsInviteSroRequest**](OrganisationsInviteSroRequest.md)|  | |

### Return type

[**OrganisationsInviteSro201Response**](OrganisationsInviteSro201Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created |  -  |
| **400** | Invalid argument(s) |  -  |
| **403** | Forbidden |  -  |
| **409** | The email already belongs to a user; appoint an existing member with PUT /organisations/{id}/sro instead |  -  |

<a id="organisationsRemoveDelegate"></a>
# **organisationsRemoveDelegate**
> OrganisationsAppointSro200Response organisationsRemoveDelegate(id, userId)

organisations@removeDelegate

Detaches a delegate from the organisation and notifies them and the remaining members. The SRO and delegates of the organisation can remove other delegates; the SRO cannot be removed and nobody can remove themselves.

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
    Integer userId = 1; // Integer | ID of the delegate to remove
    try {
      OrganisationsAppointSro200Response result = apiInstance.organisationsRemoveDelegate(id, userId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrganisationsApi#organisationsRemoveDelegate");
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
| **userId** | **Integer**| ID of the delegate to remove | |

### Return type

[**OrganisationsAppointSro200Response**](OrganisationsAppointSro200Response.md)

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
| **403** | Forbidden |  -  |
| **404** | The user is not a delegate of this organisation |  -  |

<a id="organisationsResendSroInvite"></a>
# **organisationsResendSroInvite**
> OrganisationsAppointSro200Response organisationsResendSroInvite(id)

organisations@resendSroInvite

Resends the pending SRO invitation with the code it already has. Delegates can resend while the organisation has no claimed SRO; after that only the SRO can.

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
      OrganisationsAppointSro200Response result = apiInstance.organisationsResendSroInvite(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrganisationsApi#organisationsResendSroInvite");
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

[**OrganisationsAppointSro200Response**](OrganisationsAppointSro200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **403** | Forbidden |  -  |
| **404** | The organisation has no pending SRO invitation |  -  |

