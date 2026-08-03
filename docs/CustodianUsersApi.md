# CustodianUsersApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**custodianUsersIndex**](CustodianUsersApi.md#custodianUsersIndex) | **GET** /api/v1/custodian_users | Return a list of Custodian Users |


<a id="custodianUsersIndex"></a>
# **custodianUsersIndex**
> CustodianUsersIndex200Response custodianUsersIndex()

Return a list of Custodian Users

Return a list of Custodian Users

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.CustodianUsersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CustodianUsersApi apiInstance = new CustodianUsersApi(defaultClient);
    try {
      CustodianUsersIndex200Response result = apiInstance.custodianUsersIndex();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustodianUsersApi#custodianUsersIndex");
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

[**CustodianUsersIndex200Response**](CustodianUsersIndex200Response.md)

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

