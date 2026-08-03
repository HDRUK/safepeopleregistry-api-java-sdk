# ProjectUserApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**projectUserShow**](ProjectUserApi.md#projectUserShow) | **GET** /api/v1/project_users/{id} | Get project user details |


<a id="projectUserShow"></a>
# **projectUserShow**
> CustodianProjectUsersShow200Response projectUserShow(id)

Get project user details

Returns details for a specific project user

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ProjectUserApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ProjectUserApi apiInstance = new ProjectUserApi(defaultClient);
    Integer id = 56; // Integer | ID of the project user
    try {
      CustodianProjectUsersShow200Response result = apiInstance.projectUserShow(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProjectUserApi#projectUserShow");
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
| **id** | **Integer**| ID of the project user | |

### Return type

[**CustodianProjectUsersShow200Response**](CustodianProjectUsersShow200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful operation |  -  |
| **400** | Invalid argument(s) |  -  |
| **403** | Forbidden |  -  |
| **404** | Not Found |  -  |

