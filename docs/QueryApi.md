# QueryApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**queryQuery**](QueryApi.md#queryQuery) | **POST** /api/v1/query | Query@query |


<a id="queryQuery"></a>
# **queryQuery**
> QueryQuery200Response queryQuery(xClientId, queryQueryRequest)

Query@query

Query the registry by Digital Identifier

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.QueryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    QueryApi apiInstance = new QueryApi(defaultClient);
    String xClientId = "8f14e45f-ceea-467e-adc1-0000example"; // String | Custodian client ID used to authenticate the requesting custodian
    QueryQueryRequest queryQueryRequest = new QueryQueryRequest(); // QueryQueryRequest | Query definition
    try {
      QueryQuery200Response result = apiInstance.queryQuery(xClientId, queryQueryRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling QueryApi#queryQuery");
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
| **xClientId** | **String**| Custodian client ID used to authenticate the requesting custodian | |
| **queryQueryRequest** | [**QueryQueryRequest**](QueryQueryRequest.md)| Query definition | |

### Return type

[**QueryQuery200Response**](QueryQuery200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthorised - missing or unrecognised x-client-id header |  -  |
| **404** | Not found response |  -  |
| **200** | Success |  -  |

