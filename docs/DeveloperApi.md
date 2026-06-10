# Solifyn.Api.DeveloperApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**DeveloperCreateApiKey**](DeveloperApi.md#developercreateapikey) | **POST** /v1/developer/api-keys | Create Developer API Key |
| [**DeveloperCreateWebhook**](DeveloperApi.md#developercreatewebhook) | **POST** /v1/developer/webhooks | Create Webhook Endpoint |
| [**DeveloperDeleteWebhook**](DeveloperApi.md#developerdeletewebhook) | **DELETE** /v1/developer/webhooks/{id} | Delete Webhook Endpoint |
| [**DeveloperGetAppPortal**](DeveloperApi.md#developergetappportal) | **GET** /v1/developer/webhooks/app-portal | Retrieve Hosted Webhooks Portal URL |
| [**DeveloperGetWebhook**](DeveloperApi.md#developergetwebhook) | **GET** /v1/developer/webhooks/{id} | Retrieve Webhook Endpoint Details |
| [**DeveloperListApiKeys**](DeveloperApi.md#developerlistapikeys) | **GET** /v1/developer/api-keys | List Developer API Keys |
| [**DeveloperListWebhookDeliveries**](DeveloperApi.md#developerlistwebhookdeliveries) | **GET** /v1/developer/webhooks/{id}/deliveries | Retrieve Webhook Delivery Logs |
| [**DeveloperListWebhooks**](DeveloperApi.md#developerlistwebhooks) | **GET** /v1/developer/webhooks | List Webhook Endpoints |
| [**DeveloperRevokeApiKey**](DeveloperApi.md#developerrevokeapikey) | **DELETE** /v1/developer/api-keys/{id} | Revoke API Key |
| [**DeveloperUpdateWebhook**](DeveloperApi.md#developerupdatewebhook) | **PATCH** /v1/developer/webhooks/{id} | Update Webhook Endpoint |

<a id="developercreateapikey"></a>
# **DeveloperCreateApiKey**
> ApiKeyResponseDto DeveloperCreateApiKey (CreateApiKeyDto createApiKeyDto)

Create Developer API Key

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class DeveloperCreateApiKeyExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            var apiInstance = new DeveloperApi(config);
            var createApiKeyDto = new CreateApiKeyDto(); // CreateApiKeyDto | 

            try
            {
                // Create Developer API Key
                ApiKeyResponseDto result = apiInstance.DeveloperCreateApiKey(createApiKeyDto);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeveloperApi.DeveloperCreateApiKey: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeveloperCreateApiKeyWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Developer API Key
    ApiResponse<ApiKeyResponseDto> response = apiInstance.DeveloperCreateApiKeyWithHttpInfo(createApiKeyDto);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeveloperApi.DeveloperCreateApiKeyWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createApiKeyDto** | [**CreateApiKeyDto**](CreateApiKeyDto.md) |  |  |

### Return type

[**ApiKeyResponseDto**](ApiKeyResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="developercreatewebhook"></a>
# **DeveloperCreateWebhook**
> WebhookEndpointResponseDto DeveloperCreateWebhook (CreateWebhookEndpointDto createWebhookEndpointDto)

Create Webhook Endpoint

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class DeveloperCreateWebhookExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            var apiInstance = new DeveloperApi(config);
            var createWebhookEndpointDto = new CreateWebhookEndpointDto(); // CreateWebhookEndpointDto | 

            try
            {
                // Create Webhook Endpoint
                WebhookEndpointResponseDto result = apiInstance.DeveloperCreateWebhook(createWebhookEndpointDto);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeveloperApi.DeveloperCreateWebhook: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeveloperCreateWebhookWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Webhook Endpoint
    ApiResponse<WebhookEndpointResponseDto> response = apiInstance.DeveloperCreateWebhookWithHttpInfo(createWebhookEndpointDto);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeveloperApi.DeveloperCreateWebhookWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createWebhookEndpointDto** | [**CreateWebhookEndpointDto**](CreateWebhookEndpointDto.md) |  |  |

### Return type

[**WebhookEndpointResponseDto**](WebhookEndpointResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="developerdeletewebhook"></a>
# **DeveloperDeleteWebhook**
> void DeveloperDeleteWebhook (string id)

Delete Webhook Endpoint

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class DeveloperDeleteWebhookExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            var apiInstance = new DeveloperApi(config);
            var id = "id_example";  // string | The webhook endpoint ID

            try
            {
                // Delete Webhook Endpoint
                apiInstance.DeveloperDeleteWebhook(id);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeveloperApi.DeveloperDeleteWebhook: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeveloperDeleteWebhookWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete Webhook Endpoint
    apiInstance.DeveloperDeleteWebhookWithHttpInfo(id);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeveloperApi.DeveloperDeleteWebhookWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The webhook endpoint ID |  |

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

<a id="developergetappportal"></a>
# **DeveloperGetAppPortal**
> AppPortalUrlResponseDto DeveloperGetAppPortal ()

Retrieve Hosted Webhooks Portal URL

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class DeveloperGetAppPortalExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            var apiInstance = new DeveloperApi(config);

            try
            {
                // Retrieve Hosted Webhooks Portal URL
                AppPortalUrlResponseDto result = apiInstance.DeveloperGetAppPortal();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeveloperApi.DeveloperGetAppPortal: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeveloperGetAppPortalWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieve Hosted Webhooks Portal URL
    ApiResponse<AppPortalUrlResponseDto> response = apiInstance.DeveloperGetAppPortalWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeveloperApi.DeveloperGetAppPortalWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**AppPortalUrlResponseDto**](AppPortalUrlResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="developergetwebhook"></a>
# **DeveloperGetWebhook**
> WebhookEndpointResponseDto DeveloperGetWebhook (string id)

Retrieve Webhook Endpoint Details

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class DeveloperGetWebhookExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            var apiInstance = new DeveloperApi(config);
            var id = "id_example";  // string | The webhook endpoint ID

            try
            {
                // Retrieve Webhook Endpoint Details
                WebhookEndpointResponseDto result = apiInstance.DeveloperGetWebhook(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeveloperApi.DeveloperGetWebhook: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeveloperGetWebhookWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieve Webhook Endpoint Details
    ApiResponse<WebhookEndpointResponseDto> response = apiInstance.DeveloperGetWebhookWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeveloperApi.DeveloperGetWebhookWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The webhook endpoint ID |  |

### Return type

[**WebhookEndpointResponseDto**](WebhookEndpointResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="developerlistapikeys"></a>
# **DeveloperListApiKeys**
> List&lt;ApiKeyResponseDto&gt; DeveloperListApiKeys ()

List Developer API Keys

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class DeveloperListApiKeysExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            var apiInstance = new DeveloperApi(config);

            try
            {
                // List Developer API Keys
                List<ApiKeyResponseDto> result = apiInstance.DeveloperListApiKeys();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeveloperApi.DeveloperListApiKeys: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeveloperListApiKeysWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Developer API Keys
    ApiResponse<List<ApiKeyResponseDto>> response = apiInstance.DeveloperListApiKeysWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeveloperApi.DeveloperListApiKeysWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**List&lt;ApiKeyResponseDto&gt;**](ApiKeyResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="developerlistwebhookdeliveries"></a>
# **DeveloperListWebhookDeliveries**
> List&lt;WebhookDeliveryResponseDto&gt; DeveloperListWebhookDeliveries (string id)

Retrieve Webhook Delivery Logs

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class DeveloperListWebhookDeliveriesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            var apiInstance = new DeveloperApi(config);
            var id = "id_example";  // string | The webhook endpoint ID

            try
            {
                // Retrieve Webhook Delivery Logs
                List<WebhookDeliveryResponseDto> result = apiInstance.DeveloperListWebhookDeliveries(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeveloperApi.DeveloperListWebhookDeliveries: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeveloperListWebhookDeliveriesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieve Webhook Delivery Logs
    ApiResponse<List<WebhookDeliveryResponseDto>> response = apiInstance.DeveloperListWebhookDeliveriesWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeveloperApi.DeveloperListWebhookDeliveriesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The webhook endpoint ID |  |

### Return type

[**List&lt;WebhookDeliveryResponseDto&gt;**](WebhookDeliveryResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="developerlistwebhooks"></a>
# **DeveloperListWebhooks**
> List&lt;WebhookEndpointResponseDto&gt; DeveloperListWebhooks ()

List Webhook Endpoints

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class DeveloperListWebhooksExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            var apiInstance = new DeveloperApi(config);

            try
            {
                // List Webhook Endpoints
                List<WebhookEndpointResponseDto> result = apiInstance.DeveloperListWebhooks();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeveloperApi.DeveloperListWebhooks: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeveloperListWebhooksWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Webhook Endpoints
    ApiResponse<List<WebhookEndpointResponseDto>> response = apiInstance.DeveloperListWebhooksWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeveloperApi.DeveloperListWebhooksWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**List&lt;WebhookEndpointResponseDto&gt;**](WebhookEndpointResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="developerrevokeapikey"></a>
# **DeveloperRevokeApiKey**
> void DeveloperRevokeApiKey (string id)

Revoke API Key

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class DeveloperRevokeApiKeyExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            var apiInstance = new DeveloperApi(config);
            var id = "id_example";  // string | The API key ID

            try
            {
                // Revoke API Key
                apiInstance.DeveloperRevokeApiKey(id);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeveloperApi.DeveloperRevokeApiKey: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeveloperRevokeApiKeyWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Revoke API Key
    apiInstance.DeveloperRevokeApiKeyWithHttpInfo(id);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeveloperApi.DeveloperRevokeApiKeyWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The API key ID |  |

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

<a id="developerupdatewebhook"></a>
# **DeveloperUpdateWebhook**
> WebhookEndpointResponseDto DeveloperUpdateWebhook (string id, UpdateWebhookEndpointDto updateWebhookEndpointDto)

Update Webhook Endpoint

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class DeveloperUpdateWebhookExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            var apiInstance = new DeveloperApi(config);
            var id = "id_example";  // string | The webhook endpoint ID
            var updateWebhookEndpointDto = new UpdateWebhookEndpointDto(); // UpdateWebhookEndpointDto | 

            try
            {
                // Update Webhook Endpoint
                WebhookEndpointResponseDto result = apiInstance.DeveloperUpdateWebhook(id, updateWebhookEndpointDto);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeveloperApi.DeveloperUpdateWebhook: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeveloperUpdateWebhookWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Webhook Endpoint
    ApiResponse<WebhookEndpointResponseDto> response = apiInstance.DeveloperUpdateWebhookWithHttpInfo(id, updateWebhookEndpointDto);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeveloperApi.DeveloperUpdateWebhookWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The webhook endpoint ID |  |
| **updateWebhookEndpointDto** | [**UpdateWebhookEndpointDto**](UpdateWebhookEndpointDto.md) |  |  |

### Return type

[**WebhookEndpointResponseDto**](WebhookEndpointResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

