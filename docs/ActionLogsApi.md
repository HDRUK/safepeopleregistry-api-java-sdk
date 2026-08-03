# ActionLogsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**actionLogsGetEntityActionLog**](ActionLogsApi.md#actionLogsGetEntityActionLog) | **GET** /api/v1/{entity}/{id}/action_log | Get Action Logs for an Entity |
| [**actionLogsUpdate**](ActionLogsApi.md#actionLogsUpdate) | **PUT** /api/v1/action_logs/{id} | Update an Action Log |


<a id="actionLogsGetEntityActionLog"></a>
# **actionLogsGetEntityActionLog**
> ActionLogsGetEntityActionLog200Response actionLogsGetEntityActionLog(entity, id)

Get Action Logs for an Entity

Retrieve action logs for a given entity type (users, organisations) by ID.

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ActionLogsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ActionLogsApi apiInstance = new ActionLogsApi(defaultClient);
    String entity = "entity_example"; // String | The entity type (e.g., users, organisations)
    Integer id = 56; // Integer | The ID of the entity
    try {
      ActionLogsGetEntityActionLog200Response result = apiInstance.actionLogsGetEntityActionLog(entity, id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ActionLogsApi#actionLogsGetEntityActionLog");
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
| **entity** | **String**| The entity type (e.g., users, organisations) | |
| **id** | **Integer**| The ID of the entity | |

### Return type

[**ActionLogsGetEntityActionLog200Response**](ActionLogsGetEntityActionLog200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response with action logs |  -  |
| **404** | No action logs found for this entity |  -  |
| **400** | Invalid entity type |  -  |

<a id="actionLogsUpdate"></a>
# **actionLogsUpdate**
> ActionLogsUpdate200Response actionLogsUpdate(id, complete, incomplete)

Update an Action Log

Update an action log entry, including marking it as complete or incomplete.

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.ActionLogsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ActionLogsApi apiInstance = new ActionLogsApi(defaultClient);
    Integer id = 56; // Integer | ID of the action log
    Boolean complete = true; // Boolean | Mark as complete
    Boolean incomplete = true; // Boolean | Mark as incomplete
    try {
      ActionLogsUpdate200Response result = apiInstance.actionLogsUpdate(id, complete, incomplete);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ActionLogsApi#actionLogsUpdate");
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
| **id** | **Integer**| ID of the action log | |
| **complete** | **Boolean**| Mark as complete | [optional] |
| **incomplete** | **Boolean**| Mark as incomplete | [optional] |

### Return type

[**ActionLogsUpdate200Response**](ActionLogsUpdate200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Action status updated successfully |  -  |
| **404** | Action log not found |  -  |

