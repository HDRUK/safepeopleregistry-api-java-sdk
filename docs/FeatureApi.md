# FeatureApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**featureIndex**](FeatureApi.md#featureIndex) | **GET** /api/v1/features | Feature@index |
| [**featureShow**](FeatureApi.md#featureShow) | **GET** /api/v1/features/{featureId} | Feature@show |
| [**featureToggleByFeatureId**](FeatureApi.md#featureToggleByFeatureId) | **PUT** /api/v1/features/{featureId}/toggle | Feature@show |


<a id="featureIndex"></a>
# **featureIndex**
> FeatureIndex200Response featureIndex()

Feature@index

Return a list of Feature entries

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.FeatureApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    FeatureApi apiInstance = new FeatureApi(defaultClient);
    try {
      FeatureIndex200Response result = apiInstance.featureIndex();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FeatureApi#featureIndex");
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

[**FeatureIndex200Response**](FeatureIndex200Response.md)

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

<a id="featureShow"></a>
# **featureShow**
> FeatureIndex200Response featureShow(featureId)

Feature@show

Return a Feature entry by its ID

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.FeatureApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    FeatureApi apiInstance = new FeatureApi(defaultClient);
    Integer featureId = 56; // Integer | ID of the feature
    try {
      FeatureIndex200Response result = apiInstance.featureShow(featureId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FeatureApi#featureShow");
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
| **featureId** | **Integer**| ID of the feature | |

### Return type

[**FeatureIndex200Response**](FeatureIndex200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **400** | Invalid argument(s) |  -  |
| **404** | Not found response |  -  |

<a id="featureToggleByFeatureId"></a>
# **featureToggleByFeatureId**
> FeatureIndex200Response featureToggleByFeatureId(featureId)

Feature@show

Toggle and return a Feature entry by its ID

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.FeatureApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    FeatureApi apiInstance = new FeatureApi(defaultClient);
    Integer featureId = 56; // Integer | ID of the feature
    try {
      FeatureIndex200Response result = apiInstance.featureToggleByFeatureId(featureId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FeatureApi#featureToggleByFeatureId");
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
| **featureId** | **Integer**| ID of the feature | |

### Return type

[**FeatureIndex200Response**](FeatureIndex200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **400** | Invalid argument(s) |  -  |
| **404** | Not found response |  -  |

