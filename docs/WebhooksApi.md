# WebhooksApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**webhooksCreateReceiver**](WebhooksApi.md#webhooksCreateReceiver) | **POST** /api/v1/webhooks/receivers | Create a new webhook receiver |
| [**webhooksDeleteReceiver**](WebhooksApi.md#webhooksDeleteReceiver) | **DELETE** /api/v1/webhooks/receivers/{custodianId} | Delete a webhook receiver |
| [**webhooksGetAllEventTriggers**](WebhooksApi.md#webhooksGetAllEventTriggers) | **GET** /api/v1/webhooks/event-triggers | Get all webhook event triggers |
| [**webhooksGetAllReceivers**](WebhooksApi.md#webhooksGetAllReceivers) | **GET** /api/v1/webhooks/receivers | Get all webhook receivers |
| [**webhooksGetReceiversByCustodian**](WebhooksApi.md#webhooksGetReceiversByCustodian) | **GET** /api/v1/webhooks/receivers/{custodianId} | Get webhook receivers by custodian |
| [**webhooksSendgrid**](WebhooksApi.md#webhooksSendgrid) | **GET** /api/v1/webhooks/sendgrid | Get sendgrid webhook event triggers |
| [**webhooksUpdateReceiver**](WebhooksApi.md#webhooksUpdateReceiver) | **PUT** /api/v1/webhooks/receivers/{custodianId} | Update a webhook receiver |


<a id="webhooksCreateReceiver"></a>
# **webhooksCreateReceiver**
> WebhooksCreateReceiver201Response webhooksCreateReceiver(webhooksCreateReceiverRequest)

Create a new webhook receiver

Creates a new webhook receiver for a custodian

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.WebhooksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    WebhooksApi apiInstance = new WebhooksApi(defaultClient);
    WebhooksCreateReceiverRequest webhooksCreateReceiverRequest = new WebhooksCreateReceiverRequest(); // WebhooksCreateReceiverRequest | 
    try {
      WebhooksCreateReceiver201Response result = apiInstance.webhooksCreateReceiver(webhooksCreateReceiverRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhooksApi#webhooksCreateReceiver");
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
| **webhooksCreateReceiverRequest** | [**WebhooksCreateReceiverRequest**](WebhooksCreateReceiverRequest.md)|  | |

### Return type

[**WebhooksCreateReceiver201Response**](WebhooksCreateReceiver201Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Successful operation |  -  |
| **422** | Validation error |  -  |

<a id="webhooksDeleteReceiver"></a>
# **webhooksDeleteReceiver**
> EducationDestroyByRegistryId200Response webhooksDeleteReceiver(custodianId, webhooksDeleteReceiverRequest)

Delete a webhook receiver

Deletes a specific webhook receiver for a custodian

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.WebhooksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    WebhooksApi apiInstance = new WebhooksApi(defaultClient);
    Integer custodianId = 56; // Integer | 
    WebhooksDeleteReceiverRequest webhooksDeleteReceiverRequest = new WebhooksDeleteReceiverRequest(); // WebhooksDeleteReceiverRequest | 
    try {
      EducationDestroyByRegistryId200Response result = apiInstance.webhooksDeleteReceiver(custodianId, webhooksDeleteReceiverRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhooksApi#webhooksDeleteReceiver");
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
| **custodianId** | **Integer**|  | |
| **webhooksDeleteReceiverRequest** | [**WebhooksDeleteReceiverRequest**](WebhooksDeleteReceiverRequest.md)|  | |

### Return type

[**EducationDestroyByRegistryId200Response**](EducationDestroyByRegistryId200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful operation |  -  |
| **400** | Invalid argument(s) |  -  |
| **404** | Webhook receiver not found |  -  |

<a id="webhooksGetAllEventTriggers"></a>
# **webhooksGetAllEventTriggers**
> WebhooksGetAllEventTriggers200Response webhooksGetAllEventTriggers()

Get all webhook event triggers

Returns all webhook event triggers

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.WebhooksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    WebhooksApi apiInstance = new WebhooksApi(defaultClient);
    try {
      WebhooksGetAllEventTriggers200Response result = apiInstance.webhooksGetAllEventTriggers();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhooksApi#webhooksGetAllEventTriggers");
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

[**WebhooksGetAllEventTriggers200Response**](WebhooksGetAllEventTriggers200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful operation |  -  |

<a id="webhooksGetAllReceivers"></a>
# **webhooksGetAllReceivers**
> WebhooksGetAllReceivers200Response webhooksGetAllReceivers()

Get all webhook receivers

Returns all webhook receivers with their associated event trigger details

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.WebhooksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    WebhooksApi apiInstance = new WebhooksApi(defaultClient);
    try {
      WebhooksGetAllReceivers200Response result = apiInstance.webhooksGetAllReceivers();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhooksApi#webhooksGetAllReceivers");
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

[**WebhooksGetAllReceivers200Response**](WebhooksGetAllReceivers200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful operation |  -  |

<a id="webhooksGetReceiversByCustodian"></a>
# **webhooksGetReceiversByCustodian**
> WebhooksGetAllReceivers200Response webhooksGetReceiversByCustodian(custodianId)

Get webhook receivers by custodian

Returns all webhook receivers for a specific custodian with their associated event trigger details

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.WebhooksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    WebhooksApi apiInstance = new WebhooksApi(defaultClient);
    Integer custodianId = 56; // Integer | 
    try {
      WebhooksGetAllReceivers200Response result = apiInstance.webhooksGetReceiversByCustodian(custodianId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhooksApi#webhooksGetReceiversByCustodian");
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
| **custodianId** | **Integer**|  | |

### Return type

[**WebhooksGetAllReceivers200Response**](WebhooksGetAllReceivers200Response.md)

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

<a id="webhooksSendgrid"></a>
# **webhooksSendgrid**
> webhooksSendgrid()

Get sendgrid webhook event triggers

Returns sendgrid webhook event triggers

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.WebhooksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    WebhooksApi apiInstance = new WebhooksApi(defaultClient);
    try {
      apiInstance.webhooksSendgrid();
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhooksApi#webhooksSendgrid");
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

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful operation |  -  |

<a id="webhooksUpdateReceiver"></a>
# **webhooksUpdateReceiver**
> EducationDestroyByRegistryId200Response webhooksUpdateReceiver(custodianId, webhooksUpdateReceiverRequest)

Update a webhook receiver

Updates a specific webhook receiver for a custodian

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.WebhooksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    WebhooksApi apiInstance = new WebhooksApi(defaultClient);
    Integer custodianId = 56; // Integer | 
    WebhooksUpdateReceiverRequest webhooksUpdateReceiverRequest = new WebhooksUpdateReceiverRequest(); // WebhooksUpdateReceiverRequest | 
    try {
      EducationDestroyByRegistryId200Response result = apiInstance.webhooksUpdateReceiver(custodianId, webhooksUpdateReceiverRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhooksApi#webhooksUpdateReceiver");
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
| **custodianId** | **Integer**|  | |
| **webhooksUpdateReceiverRequest** | [**WebhooksUpdateReceiverRequest**](WebhooksUpdateReceiverRequest.md)|  | |

### Return type

[**EducationDestroyByRegistryId200Response**](EducationDestroyByRegistryId200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful operation |  -  |
| **400** | Invalid argument(s) |  -  |
| **404** | Webhook receiver not found |  -  |
| **422** | Validation error |  -  |

