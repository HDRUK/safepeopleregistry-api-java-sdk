# EndorsementsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**endorsementsStore**](EndorsementsApi.md#endorsementsStore) | **POST** /api/v1/endorsements | Endorsements@store |


<a id="endorsementsStore"></a>
# **endorsementsStore**
> EndorsementsStore201Response endorsementsStore(endorsementsStoreRequest)

Endorsements@store

Create an Endorsements entry

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.EndorsementsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    EndorsementsApi apiInstance = new EndorsementsApi(defaultClient);
    EndorsementsStoreRequest endorsementsStoreRequest = new EndorsementsStoreRequest(); // EndorsementsStoreRequest | Endorsements definition
    try {
      EndorsementsStore201Response result = apiInstance.endorsementsStore(endorsementsStoreRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EndorsementsApi#endorsementsStore");
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
| **endorsementsStoreRequest** | [**EndorsementsStoreRequest**](EndorsementsStoreRequest.md)| Endorsements definition | |

### Return type

[**EndorsementsStore201Response**](EndorsementsStore201Response.md)

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

