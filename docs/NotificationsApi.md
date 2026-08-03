# NotificationsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**notificationsGetNotificationCounts**](NotificationsApi.md#notificationsGetNotificationCounts) | **GET** /api/v1/users/{id}/notifications/count | Get notification counts for a specific user |
| [**notificationsGetUserNotifications**](NotificationsApi.md#notificationsGetUserNotifications) | **GET** /api/v1/users/{id}/notifications | Get notifications for a specific user |
| [**notificationsMarkUserNotificationAsRead**](NotificationsApi.md#notificationsMarkUserNotificationAsRead) | **PATCH** /api/v1/users/{id}/notifications/{notificationId}/read | Mark a specific notification as read |
| [**notificationsMarkUserNotificationAsUnread**](NotificationsApi.md#notificationsMarkUserNotificationAsUnread) | **PATCH** /api/v1/users/{id}/notifications/{notificationId}/unread | Mark a specific notification as unread |
| [**notificationsMarkUserNotificationsAsRead**](NotificationsApi.md#notificationsMarkUserNotificationsAsRead) | **PATCH** /api/v1/users/{id}/notifications/read | Mark all notifications as read for a specific user |


<a id="notificationsGetNotificationCounts"></a>
# **notificationsGetNotificationCounts**
> NotificationsGetNotificationCounts200Response notificationsGetNotificationCounts(id)

Get notification counts for a specific user

Retrieve the total, read, and unread notification counts for a given user.

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.NotificationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    NotificationsApi apiInstance = new NotificationsApi(defaultClient);
    Integer id = 56; // Integer | User ID
    try {
      NotificationsGetNotificationCounts200Response result = apiInstance.notificationsGetNotificationCounts(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NotificationsApi#notificationsGetNotificationCounts");
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
| **id** | **Integer**| User ID | |

### Return type

[**NotificationsGetNotificationCounts200Response**](NotificationsGetNotificationCounts200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |
| **401** | Unauthorized |  -  |
| **404** | User not found |  -  |

<a id="notificationsGetUserNotifications"></a>
# **notificationsGetUserNotifications**
> NotificationsGetUserNotifications200Response notificationsGetUserNotifications(id, status)

Get notifications for a specific user

Retrieves notifications for a user, with an optional filter for read/unread notifications.

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.NotificationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    NotificationsApi apiInstance = new NotificationsApi(defaultClient);
    Integer id = 1; // Integer | User ID
    String status = "read"; // String | Filter notifications by status (read/unread)
    try {
      NotificationsGetUserNotifications200Response result = apiInstance.notificationsGetUserNotifications(id, status);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NotificationsApi#notificationsGetUserNotifications");
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
| **id** | **Integer**| User ID | |
| **status** | **String**| Filter notifications by status (read/unread) | [optional] [enum: read, unread] |

### Return type

[**NotificationsGetUserNotifications200Response**](NotificationsGetUserNotifications200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful response |  -  |
| **404** | User not found |  -  |

<a id="notificationsMarkUserNotificationAsRead"></a>
# **notificationsMarkUserNotificationAsRead**
> NotificationsMarkUserNotificationAsRead200Response notificationsMarkUserNotificationAsRead(id, notificationId)

Mark a specific notification as read

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.NotificationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    NotificationsApi apiInstance = new NotificationsApi(defaultClient);
    Integer id = 1; // Integer | User ID
    String notificationId = "abc95e84-0ebd-45d2-8129-9bf7ed043433"; // String | Notification ID
    try {
      NotificationsMarkUserNotificationAsRead200Response result = apiInstance.notificationsMarkUserNotificationAsRead(id, notificationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NotificationsApi#notificationsMarkUserNotificationAsRead");
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
| **id** | **Integer**| User ID | |
| **notificationId** | **String**| Notification ID | |

### Return type

[**NotificationsMarkUserNotificationAsRead200Response**](NotificationsMarkUserNotificationAsRead200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Notification marked as read |  -  |
| **404** | User or notification not found |  -  |

<a id="notificationsMarkUserNotificationAsUnread"></a>
# **notificationsMarkUserNotificationAsUnread**
> notificationsMarkUserNotificationAsUnread(id, notificationId)

Mark a specific notification as unread

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.NotificationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    NotificationsApi apiInstance = new NotificationsApi(defaultClient);
    Integer id = 1; // Integer | User ID
    String notificationId = "abc95e84-0ebd-45d2-8129-9bf7ed043433"; // String | Notification ID
    try {
      apiInstance.notificationsMarkUserNotificationAsUnread(id, notificationId);
    } catch (ApiException e) {
      System.err.println("Exception when calling NotificationsApi#notificationsMarkUserNotificationAsUnread");
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
| **id** | **Integer**| User ID | |
| **notificationId** | **String**| Notification ID | |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Notification marked as unread |  -  |

<a id="notificationsMarkUserNotificationsAsRead"></a>
# **notificationsMarkUserNotificationsAsRead**
> NotificationsMarkUserNotificationsAsRead200Response notificationsMarkUserNotificationsAsRead(id)

Mark all notifications as read for a specific user

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.NotificationsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    NotificationsApi apiInstance = new NotificationsApi(defaultClient);
    Integer id = 1; // Integer | User ID
    try {
      NotificationsMarkUserNotificationsAsRead200Response result = apiInstance.notificationsMarkUserNotificationsAsRead(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NotificationsApi#notificationsMarkUserNotificationsAsRead");
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
| **id** | **Integer**| User ID | |

### Return type

[**NotificationsMarkUserNotificationsAsRead200Response**](NotificationsMarkUserNotificationsAsRead200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Notifications marked as read |  -  |
| **404** | User not found |  -  |

