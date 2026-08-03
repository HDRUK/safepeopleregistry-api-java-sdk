# CustodianModelConfigApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**custodianModelConfigDestroy**](CustodianModelConfigApi.md#custodianModelConfigDestroy) | **DELETE** /api/v1/custodian_config/{id} | CustodianModelConfig@destroy |
| [**custodianModelConfigGetByCustodianID**](CustodianModelConfigApi.md#custodianModelConfigGetByCustodianID) | **GET** /api/v1/custodian_config/{id} | CustodianModelConfig@getByCustodianID |
| [**custodianModelConfigGetEntityModels**](CustodianModelConfigApi.md#custodianModelConfigGetEntityModels) | **GET** /api/v1/custodian_config/{custodianId}/entity_models | Get entity models for custodian config |
| [**custodianModelConfigStore**](CustodianModelConfigApi.md#custodianModelConfigStore) | **POST** /api/v1/custodian_config | CustodianModelConfig@store |
| [**custodianModelConfigUpdate**](CustodianModelConfigApi.md#custodianModelConfigUpdate) | **PUT** /api/v1/custodian_config/{id} | CustodianModelConfig@update |
| [**custodianModelConfigUpdateEntityModels**](CustodianModelConfigApi.md#custodianModelConfigUpdateEntityModels) | **PUT** /api/v1/custodian_config/{custodianId}/entity_models | Update a custodian&#39;s entity models |


<a id="custodianModelConfigDestroy"></a>
# **custodianModelConfigDestroy**
> AffiliationDestroy200Response custodianModelConfigDestroy(id)

CustodianModelConfig@destroy

Delete a CustodianModelConfig entry from the system

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.CustodianModelConfigApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CustodianModelConfigApi apiInstance = new CustodianModelConfigApi(defaultClient);
    Integer id = 1; // Integer | CustodianModelConfig entry ID
    try {
      AffiliationDestroy200Response result = apiInstance.custodianModelConfigDestroy(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustodianModelConfigApi#custodianModelConfigDestroy");
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
| **id** | **Integer**| CustodianModelConfig entry ID | |

### Return type

[**AffiliationDestroy200Response**](AffiliationDestroy200Response.md)

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
| **500** | Error |  -  |

<a id="custodianModelConfigGetByCustodianID"></a>
# **custodianModelConfigGetByCustodianID**
> CustodianModelConfigGetByCustodianID200Response custodianModelConfigGetByCustodianID(id)

CustodianModelConfig@getByCustodianID

Return a list of Custodian config

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.CustodianModelConfigApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CustodianModelConfigApi apiInstance = new CustodianModelConfigApi(defaultClient);
    Integer id = 1; // Integer | CustodianModelConfig entry ID
    try {
      CustodianModelConfigGetByCustodianID200Response result = apiInstance.custodianModelConfigGetByCustodianID(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustodianModelConfigApi#custodianModelConfigGetByCustodianID");
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
| **id** | **Integer**| CustodianModelConfig entry ID | |

### Return type

[**CustodianModelConfigGetByCustodianID200Response**](CustodianModelConfigGetByCustodianID200Response.md)

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

<a id="custodianModelConfigGetEntityModels"></a>
# **custodianModelConfigGetEntityModels**
> CustodianModelConfigGetEntityModels200Response custodianModelConfigGetEntityModels(custodianId, entityModelType)

Get entity models for custodian config

Retrieve entity models associated with custodian config based on the specified entity_model_type

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.CustodianModelConfigApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CustodianModelConfigApi apiInstance = new CustodianModelConfigApi(defaultClient);
    Integer custodianId = 56; // Integer | ID of the custodian
    String entityModelType = "decision_model"; // String | Type of entity model to retrieve
    try {
      CustodianModelConfigGetEntityModels200Response result = apiInstance.custodianModelConfigGetEntityModels(custodianId, entityModelType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustodianModelConfigApi#custodianModelConfigGetEntityModels");
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
| **custodianId** | **Integer**| ID of the custodian | |
| **entityModelType** | **String**| Type of entity model to retrieve | [enum: decision_model, user_validation_rules, org_validation_rules] |

### Return type

[**CustodianModelConfigGetEntityModels200Response**](CustodianModelConfigGetEntityModels200Response.md)

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

<a id="custodianModelConfigStore"></a>
# **custodianModelConfigStore**
> CustodianModelConfigUpdate200Response custodianModelConfigStore(custodianModelConfig)

CustodianModelConfig@store

Create a CustodianModelConfig entry

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.CustodianModelConfigApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CustodianModelConfigApi apiInstance = new CustodianModelConfigApi(defaultClient);
    CustodianModelConfig custodianModelConfig = new CustodianModelConfig(); // CustodianModelConfig | CustodianModelConfig definition
    try {
      CustodianModelConfigUpdate200Response result = apiInstance.custodianModelConfigStore(custodianModelConfig);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustodianModelConfigApi#custodianModelConfigStore");
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
| **custodianModelConfig** | [**CustodianModelConfig**](CustodianModelConfig.md)| CustodianModelConfig definition | |

### Return type

[**CustodianModelConfigUpdate200Response**](CustodianModelConfigUpdate200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **404** | Not found response |  -  |
| **200** | Success |  -  |
| **500** | Error |  -  |

<a id="custodianModelConfigUpdate"></a>
# **custodianModelConfigUpdate**
> CustodianModelConfigUpdate200Response custodianModelConfigUpdate(id, custodianModelConfig)

CustodianModelConfig@update

Update an CustodianModelConfig entry

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.CustodianModelConfigApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CustodianModelConfigApi apiInstance = new CustodianModelConfigApi(defaultClient);
    Integer id = 1; // Integer | CustodianModelConfig entry ID
    CustodianModelConfig custodianModelConfig = new CustodianModelConfig(); // CustodianModelConfig | CustodianModelConfig definition
    try {
      CustodianModelConfigUpdate200Response result = apiInstance.custodianModelConfigUpdate(id, custodianModelConfig);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustodianModelConfigApi#custodianModelConfigUpdate");
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
| **id** | **Integer**| CustodianModelConfig entry ID | |
| **custodianModelConfig** | [**CustodianModelConfig**](CustodianModelConfig.md)| CustodianModelConfig definition | |

### Return type

[**CustodianModelConfigUpdate200Response**](CustodianModelConfigUpdate200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **400** | Invalid argument(s) |  -  |
| **404** | Not found response |  -  |
| **200** | Success |  -  |
| **500** | Error |  -  |

<a id="custodianModelConfigUpdateEntityModels"></a>
# **custodianModelConfigUpdateEntityModels**
> CustodianModelConfigUpdateEntityModels200Response custodianModelConfigUpdateEntityModels(custodianId, custodianModelConfigUpdateEntityModelsRequest)

Update a custodian&#39;s entity models

Update the active status of specified custodian model configs for a given custodian

### Example
```java
// Import classes:
import uk.ac.hdruk.safepeopleregistryapi.ApiClient;
import uk.ac.hdruk.safepeopleregistryapi.ApiException;
import uk.ac.hdruk.safepeopleregistryapi.Configuration;
import uk.ac.hdruk.safepeopleregistryapi.models.*;
import uk.ac.hdruk.safepeopleregistryapi.api.CustodianModelConfigApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    CustodianModelConfigApi apiInstance = new CustodianModelConfigApi(defaultClient);
    Integer custodianId = 56; // Integer | ID of the custodian
    CustodianModelConfigUpdateEntityModelsRequest custodianModelConfigUpdateEntityModelsRequest = new CustodianModelConfigUpdateEntityModelsRequest(); // CustodianModelConfigUpdateEntityModelsRequest | 
    try {
      CustodianModelConfigUpdateEntityModels200Response result = apiInstance.custodianModelConfigUpdateEntityModels(custodianId, custodianModelConfigUpdateEntityModelsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustodianModelConfigApi#custodianModelConfigUpdateEntityModels");
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
| **custodianId** | **Integer**| ID of the custodian | |
| **custodianModelConfigUpdateEntityModelsRequest** | [**CustodianModelConfigUpdateEntityModelsRequest**](CustodianModelConfigUpdateEntityModelsRequest.md)|  | |

### Return type

[**CustodianModelConfigUpdateEntityModels200Response**](CustodianModelConfigUpdateEntityModels200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **400** | Invalid argument(s) |  -  |
| **404** | Not Found |  -  |

