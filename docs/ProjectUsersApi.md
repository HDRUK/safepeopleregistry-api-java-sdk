# ProjectUsersApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**projectUsersBulkInviteProjectUsers**](ProjectUsersApi.md#projectUsersBulkInviteProjectUsers) | **POST** /api/v1/project_users/bulk | Bulk invite Project Users |


<a id="projectUsersBulkInviteProjectUsers"></a>
# **projectUsersBulkInviteProjectUsers**
> projectUsersBulkInviteProjectUsers(projectUsersBulkInviteProjectUsersRequest)

Bulk invite Project Users

Invite multiple users and attach them to a project

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ProjectUsersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ProjectUsersApi apiInstance = new ProjectUsersApi(defaultClient);
    ProjectUsersBulkInviteProjectUsersRequest projectUsersBulkInviteProjectUsersRequest = new ProjectUsersBulkInviteProjectUsersRequest(); // ProjectUsersBulkInviteProjectUsersRequest | 
    try {
      apiInstance.projectUsersBulkInviteProjectUsers(projectUsersBulkInviteProjectUsersRequest);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProjectUsersApi#projectUsersBulkInviteProjectUsers");
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
| **projectUsersBulkInviteProjectUsersRequest** | [**ProjectUsersBulkInviteProjectUsersRequest**](ProjectUsersBulkInviteProjectUsersRequest.md)|  | |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Success |  -  |

