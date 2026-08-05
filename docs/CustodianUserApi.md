# CustodianUserApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**custodianUserBulkStore**](CustodianUserApi.md#custodianUserBulkStore) | **POST** /api/v1/custodian_users/bulk | Create multiple CustodianUser entries |


<a id="custodianUserBulkStore"></a>
# **custodianUserBulkStore**
> CustodianUserBulkStore201Response custodianUserBulkStore(custodianUserBulkStoreRequest)

Create multiple CustodianUser entries

Create multiple CustodianUser entries

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.CustodianUserApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CustodianUserApi apiInstance = new CustodianUserApi(defaultClient);
    CustodianUserBulkStoreRequest custodianUserBulkStoreRequest = new CustodianUserBulkStoreRequest(); // CustodianUserBulkStoreRequest | Array of CustodianUser definitions
    try {
      CustodianUserBulkStore201Response result = apiInstance.custodianUserBulkStore(custodianUserBulkStoreRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustodianUserApi#custodianUserBulkStore");
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
| **custodianUserBulkStoreRequest** | [**CustodianUserBulkStoreRequest**](CustodianUserBulkStoreRequest.md)| Array of CustodianUser definitions | |

### Return type

[**CustodianUserBulkStore201Response**](CustodianUserBulkStore201Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Success |  -  |
| **500** | Error |  -  |

