# EndorsementApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**endorsementIndex**](EndorsementApi.md#endorsementIndex) | **GET** /api/v1/endorsements | Endorsement@index |
| [**endorsementShow**](EndorsementApi.md#endorsementShow) | **GET** /api/v1/endorsements/{id} | Endorsement@show |


<a id="endorsementIndex"></a>
# **endorsementIndex**
> EndorsementIndex200Response endorsementIndex()

Endorsement@index

Return a list of Endorsements

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.EndorsementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    EndorsementApi apiInstance = new EndorsementApi(defaultClient);
    try {
      EndorsementIndex200Response result = apiInstance.endorsementIndex();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EndorsementApi#endorsementIndex");
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

[**EndorsementIndex200Response**](EndorsementIndex200Response.md)

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

<a id="endorsementShow"></a>
# **endorsementShow**
> EndorsementIndex200Response endorsementShow(id)

Endorsement@show

Return an Endorsement entry by ID

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.EndorsementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    EndorsementApi apiInstance = new EndorsementApi(defaultClient);
    Integer id = 1; // Integer | Endorsement entry ID
    try {
      EndorsementIndex200Response result = apiInstance.endorsementShow(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EndorsementApi#endorsementShow");
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
| **id** | **Integer**| Endorsement entry ID | |

### Return type

[**EndorsementIndex200Response**](EndorsementIndex200Response.md)

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

