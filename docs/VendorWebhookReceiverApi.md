# VendorWebhookReceiverApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**vendorWebhookReceiverReceive**](VendorWebhookReceiverApi.md#vendorWebhookReceiverReceive) | **POST** /api/v1/vendor-webhooks/{provider} | Receive a webhook callback from a vendor |


<a id="vendorWebhookReceiverReceive"></a>
# **vendorWebhookReceiverReceive**
> VendorWebhookReceiverReceive200Response vendorWebhookReceiverReceive(provider, body)

Receive a webhook callback from a vendor

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.VendorWebhookReceiverApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    VendorWebhookReceiverApi apiInstance = new VendorWebhookReceiverApi(defaultClient);
    String provider = "example-provider"; // String | Name of the vendor providing the webhook
    Object body = {"event":"user.created","data":{"id":123,"name":"John Doe"}}; // Object | 
    try {
      VendorWebhookReceiverReceive200Response result = apiInstance.vendorWebhookReceiverReceive(provider, body);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling VendorWebhookReceiverApi#vendorWebhookReceiverReceive");
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
| **provider** | **String**| Name of the vendor providing the webhook | |
| **body** | **Object**|  | |

### Return type

[**VendorWebhookReceiverReceive200Response**](VendorWebhookReceiverReceive200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook processed successfully |  -  |
| **400** | Invalid argument(s) |  -  |
| **500** | Internal server error |  -  |

