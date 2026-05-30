# Solifyn.Api.DeveloperApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**DeveloperControllerCreateApiKey**](DeveloperApi.md#developercontrollercreateapikey) | **POST** /v1/developer/api-keys |  |
| [**DeveloperControllerCreateWebhookEndpoint**](DeveloperApi.md#developercontrollercreatewebhookendpoint) | **POST** /v1/developer/webhooks |  |
| [**DeveloperControllerDeleteApiKey**](DeveloperApi.md#developercontrollerdeleteapikey) | **DELETE** /v1/developer/api-keys/{id} |  |
| [**DeveloperControllerDeleteWebhookEndpoint**](DeveloperApi.md#developercontrollerdeletewebhookendpoint) | **DELETE** /v1/developer/webhooks/{id} |  |
| [**DeveloperControllerGetApiKeys**](DeveloperApi.md#developercontrollergetapikeys) | **GET** /v1/developer/api-keys |  |
| [**DeveloperControllerGetAppPortalUrl**](DeveloperApi.md#developercontrollergetappportalurl) | **GET** /v1/developer/webhooks/app-portal |  |
| [**DeveloperControllerGetWebhookDeliveries**](DeveloperApi.md#developercontrollergetwebhookdeliveries) | **GET** /v1/developer/webhooks/{id}/deliveries |  |
| [**DeveloperControllerGetWebhookEndpoints**](DeveloperApi.md#developercontrollergetwebhookendpoints) | **GET** /v1/developer/webhooks |  |
| [**DeveloperControllerUpdateWebhookEndpoint**](DeveloperApi.md#developercontrollerupdatewebhookendpoint) | **PATCH** /v1/developer/webhooks/{id} |  |

<a id="developercontrollercreateapikey"></a>
# **DeveloperControllerCreateApiKey**
> void DeveloperControllerCreateApiKey ()



### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class DeveloperControllerCreateApiKeyExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            var apiInstance = new DeveloperApi(config);

            try
            {
                apiInstance.DeveloperControllerCreateApiKey();
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeveloperApi.DeveloperControllerCreateApiKey: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeveloperControllerCreateApiKeyWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.DeveloperControllerCreateApiKeyWithHttpInfo();
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeveloperApi.DeveloperControllerCreateApiKeyWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="developercontrollercreatewebhookendpoint"></a>
# **DeveloperControllerCreateWebhookEndpoint**
> void DeveloperControllerCreateWebhookEndpoint ()



### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class DeveloperControllerCreateWebhookEndpointExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            var apiInstance = new DeveloperApi(config);

            try
            {
                apiInstance.DeveloperControllerCreateWebhookEndpoint();
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeveloperApi.DeveloperControllerCreateWebhookEndpoint: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeveloperControllerCreateWebhookEndpointWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.DeveloperControllerCreateWebhookEndpointWithHttpInfo();
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeveloperApi.DeveloperControllerCreateWebhookEndpointWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="developercontrollerdeleteapikey"></a>
# **DeveloperControllerDeleteApiKey**
> void DeveloperControllerDeleteApiKey (string id)



### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class DeveloperControllerDeleteApiKeyExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            var apiInstance = new DeveloperApi(config);
            var id = "id_example";  // string | 

            try
            {
                apiInstance.DeveloperControllerDeleteApiKey(id);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeveloperApi.DeveloperControllerDeleteApiKey: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeveloperControllerDeleteApiKeyWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.DeveloperControllerDeleteApiKeyWithHttpInfo(id);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeveloperApi.DeveloperControllerDeleteApiKeyWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="developercontrollerdeletewebhookendpoint"></a>
# **DeveloperControllerDeleteWebhookEndpoint**
> void DeveloperControllerDeleteWebhookEndpoint (string id)



### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class DeveloperControllerDeleteWebhookEndpointExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            var apiInstance = new DeveloperApi(config);
            var id = "id_example";  // string | 

            try
            {
                apiInstance.DeveloperControllerDeleteWebhookEndpoint(id);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeveloperApi.DeveloperControllerDeleteWebhookEndpoint: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeveloperControllerDeleteWebhookEndpointWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.DeveloperControllerDeleteWebhookEndpointWithHttpInfo(id);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeveloperApi.DeveloperControllerDeleteWebhookEndpointWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="developercontrollergetapikeys"></a>
# **DeveloperControllerGetApiKeys**
> void DeveloperControllerGetApiKeys ()



### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class DeveloperControllerGetApiKeysExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            var apiInstance = new DeveloperApi(config);

            try
            {
                apiInstance.DeveloperControllerGetApiKeys();
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeveloperApi.DeveloperControllerGetApiKeys: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeveloperControllerGetApiKeysWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.DeveloperControllerGetApiKeysWithHttpInfo();
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeveloperApi.DeveloperControllerGetApiKeysWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="developercontrollergetappportalurl"></a>
# **DeveloperControllerGetAppPortalUrl**
> void DeveloperControllerGetAppPortalUrl ()



### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class DeveloperControllerGetAppPortalUrlExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            var apiInstance = new DeveloperApi(config);

            try
            {
                apiInstance.DeveloperControllerGetAppPortalUrl();
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeveloperApi.DeveloperControllerGetAppPortalUrl: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeveloperControllerGetAppPortalUrlWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.DeveloperControllerGetAppPortalUrlWithHttpInfo();
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeveloperApi.DeveloperControllerGetAppPortalUrlWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="developercontrollergetwebhookdeliveries"></a>
# **DeveloperControllerGetWebhookDeliveries**
> void DeveloperControllerGetWebhookDeliveries (string id)



### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class DeveloperControllerGetWebhookDeliveriesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            var apiInstance = new DeveloperApi(config);
            var id = "id_example";  // string | 

            try
            {
                apiInstance.DeveloperControllerGetWebhookDeliveries(id);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeveloperApi.DeveloperControllerGetWebhookDeliveries: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeveloperControllerGetWebhookDeliveriesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.DeveloperControllerGetWebhookDeliveriesWithHttpInfo(id);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeveloperApi.DeveloperControllerGetWebhookDeliveriesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="developercontrollergetwebhookendpoints"></a>
# **DeveloperControllerGetWebhookEndpoints**
> void DeveloperControllerGetWebhookEndpoints ()



### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class DeveloperControllerGetWebhookEndpointsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            var apiInstance = new DeveloperApi(config);

            try
            {
                apiInstance.DeveloperControllerGetWebhookEndpoints();
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeveloperApi.DeveloperControllerGetWebhookEndpoints: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeveloperControllerGetWebhookEndpointsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.DeveloperControllerGetWebhookEndpointsWithHttpInfo();
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeveloperApi.DeveloperControllerGetWebhookEndpointsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="developercontrollerupdatewebhookendpoint"></a>
# **DeveloperControllerUpdateWebhookEndpoint**
> void DeveloperControllerUpdateWebhookEndpoint (string id)



### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class DeveloperControllerUpdateWebhookEndpointExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            var apiInstance = new DeveloperApi(config);
            var id = "id_example";  // string | 

            try
            {
                apiInstance.DeveloperControllerUpdateWebhookEndpoint(id);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeveloperApi.DeveloperControllerUpdateWebhookEndpoint: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeveloperControllerUpdateWebhookEndpointWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.DeveloperControllerUpdateWebhookEndpointWithHttpInfo(id);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeveloperApi.DeveloperControllerUpdateWebhookEndpointWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

