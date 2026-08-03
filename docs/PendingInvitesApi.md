# PendingInvitesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**pendingInvitesIndex**](PendingInvitesApi.md#pendingInvitesIndex) | **GET** /api/v1/pending_invites | PendingInvite@index |


<a id="pendingInvitesIndex"></a>
# **pendingInvitesIndex**
> PendingInvitesIndex200Response pendingInvitesIndex()

PendingInvite@index

Return a list of pending invites

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.PendingInvitesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    PendingInvitesApi apiInstance = new PendingInvitesApi(defaultClient);
    try {
      PendingInvitesIndex200Response result = apiInstance.pendingInvitesIndex();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PendingInvitesApi#pendingInvitesIndex");
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

[**PendingInvitesIndex200Response**](PendingInvitesIndex200Response.md)

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

