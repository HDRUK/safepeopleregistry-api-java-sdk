# ProfessionalRegistrationsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**professionalRegistrationsUpdate**](ProfessionalRegistrationsApi.md#professionalRegistrationsUpdate) | **PUT** /api/v1/professional_registrations/{id} | Professional Registrations@update |


<a id="professionalRegistrationsUpdate"></a>
# **professionalRegistrationsUpdate**
> ProfessionalRegistrationsUpdate200Response professionalRegistrationsUpdate(id, professionalRegistrationsUpdateRequest)

Professional Registrations@update

Update a Professional Registrations entry

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ProfessionalRegistrationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ProfessionalRegistrationsApi apiInstance = new ProfessionalRegistrationsApi(defaultClient);
    Integer id = 1; // Integer | Professional Registrations entry ID
    ProfessionalRegistrationsUpdateRequest professionalRegistrationsUpdateRequest = new ProfessionalRegistrationsUpdateRequest(); // ProfessionalRegistrationsUpdateRequest | Professional Registrations definition
    try {
      ProfessionalRegistrationsUpdate200Response result = apiInstance.professionalRegistrationsUpdate(id, professionalRegistrationsUpdateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProfessionalRegistrationsApi#professionalRegistrationsUpdate");
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
| **id** | **Integer**| Professional Registrations entry ID | |
| **professionalRegistrationsUpdateRequest** | [**ProfessionalRegistrationsUpdateRequest**](ProfessionalRegistrationsUpdateRequest.md)| Professional Registrations definition | |

### Return type

[**ProfessionalRegistrationsUpdate200Response**](ProfessionalRegistrationsUpdate200Response.md)

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

