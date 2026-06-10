# Solifyn.Api.WebhookEndpointApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**OperationalWebhookControllerCreate**](WebhookEndpointApi.md#operationalwebhookcontrollercreate) | **POST** /v1/operational-webhook/endpoint | Create Operational Webhook Endpoint |
| [**OperationalWebhookControllerDelete**](WebhookEndpointApi.md#operationalwebhookcontrollerdelete) | **DELETE** /v1/operational-webhook/endpoint/{id} | Delete Operational Webhook Endpoint |
| [**OperationalWebhookControllerGet**](WebhookEndpointApi.md#operationalwebhookcontrollerget) | **GET** /v1/operational-webhook/endpoint/{id} | Get Operational Webhook Endpoint |
| [**OperationalWebhookControllerGetHeaders**](WebhookEndpointApi.md#operationalwebhookcontrollergetheaders) | **GET** /v1/operational-webhook/endpoint/{id}/headers | Get Operational Webhook Endpoint Headers |
| [**OperationalWebhookControllerGetSecret**](WebhookEndpointApi.md#operationalwebhookcontrollergetsecret) | **GET** /v1/operational-webhook/endpoint/{id}/secret | Get Operational Webhook Endpoint Secret |
| [**OperationalWebhookControllerList**](WebhookEndpointApi.md#operationalwebhookcontrollerlist) | **GET** /v1/operational-webhook/endpoint | List Operational Webhook Endpoints |
| [**OperationalWebhookControllerRotateSecret**](WebhookEndpointApi.md#operationalwebhookcontrollerrotatesecret) | **POST** /v1/operational-webhook/endpoint/{id}/secret/rotate | Rotate Operational Webhook Endpoint Secret |
| [**OperationalWebhookControllerUpdate**](WebhookEndpointApi.md#operationalwebhookcontrollerupdate) | **PUT** /v1/operational-webhook/endpoint/{id} | Update Operational Webhook Endpoint |
| [**OperationalWebhookControllerUpdateHeaders**](WebhookEndpointApi.md#operationalwebhookcontrollerupdateheaders) | **PUT** /v1/operational-webhook/endpoint/{id}/headers | Set Operational Webhook Endpoint Headers |

<a id="operationalwebhookcontrollercreate"></a>
# **OperationalWebhookControllerCreate**
> OperationalWebhookEndpointResponseDto OperationalWebhookControllerCreate (OperationalWebhookEndpointInDto operationalWebhookEndpointInDto)

Create Operational Webhook Endpoint

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class OperationalWebhookControllerCreateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new WebhookEndpointApi(config);
            var operationalWebhookEndpointInDto = new OperationalWebhookEndpointInDto(); // OperationalWebhookEndpointInDto | 

            try
            {
                // Create Operational Webhook Endpoint
                OperationalWebhookEndpointResponseDto result = apiInstance.OperationalWebhookControllerCreate(operationalWebhookEndpointInDto);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEndpointApi.OperationalWebhookControllerCreate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OperationalWebhookControllerCreateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Operational Webhook Endpoint
    ApiResponse<OperationalWebhookEndpointResponseDto> response = apiInstance.OperationalWebhookControllerCreateWithHttpInfo(operationalWebhookEndpointInDto);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEndpointApi.OperationalWebhookControllerCreateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **operationalWebhookEndpointInDto** | [**OperationalWebhookEndpointInDto**](OperationalWebhookEndpointInDto.md) |  |  |

### Return type

[**OperationalWebhookEndpointResponseDto**](OperationalWebhookEndpointResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="operationalwebhookcontrollerdelete"></a>
# **OperationalWebhookControllerDelete**
> void OperationalWebhookControllerDelete (string id)

Delete Operational Webhook Endpoint

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class OperationalWebhookControllerDeleteExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new WebhookEndpointApi(config);
            var id = "id_example";  // string | The endpoint ID or UID

            try
            {
                // Delete Operational Webhook Endpoint
                apiInstance.OperationalWebhookControllerDelete(id);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEndpointApi.OperationalWebhookControllerDelete: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OperationalWebhookControllerDeleteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete Operational Webhook Endpoint
    apiInstance.OperationalWebhookControllerDeleteWithHttpInfo(id);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEndpointApi.OperationalWebhookControllerDeleteWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The endpoint ID or UID |  |

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Deleted |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="operationalwebhookcontrollerget"></a>
# **OperationalWebhookControllerGet**
> OperationalWebhookEndpointResponseDto OperationalWebhookControllerGet (string id)

Get Operational Webhook Endpoint

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class OperationalWebhookControllerGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new WebhookEndpointApi(config);
            var id = "id_example";  // string | The endpoint ID or UID

            try
            {
                // Get Operational Webhook Endpoint
                OperationalWebhookEndpointResponseDto result = apiInstance.OperationalWebhookControllerGet(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEndpointApi.OperationalWebhookControllerGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OperationalWebhookControllerGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Operational Webhook Endpoint
    ApiResponse<OperationalWebhookEndpointResponseDto> response = apiInstance.OperationalWebhookControllerGetWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEndpointApi.OperationalWebhookControllerGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The endpoint ID or UID |  |

### Return type

[**OperationalWebhookEndpointResponseDto**](OperationalWebhookEndpointResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="operationalwebhookcontrollergetheaders"></a>
# **OperationalWebhookControllerGetHeaders**
> OperationalWebhookEndpointHeadersResponseDto OperationalWebhookControllerGetHeaders (string id)

Get Operational Webhook Endpoint Headers

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class OperationalWebhookControllerGetHeadersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new WebhookEndpointApi(config);
            var id = "id_example";  // string | The endpoint ID or UID

            try
            {
                // Get Operational Webhook Endpoint Headers
                OperationalWebhookEndpointHeadersResponseDto result = apiInstance.OperationalWebhookControllerGetHeaders(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEndpointApi.OperationalWebhookControllerGetHeaders: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OperationalWebhookControllerGetHeadersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Operational Webhook Endpoint Headers
    ApiResponse<OperationalWebhookEndpointHeadersResponseDto> response = apiInstance.OperationalWebhookControllerGetHeadersWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEndpointApi.OperationalWebhookControllerGetHeadersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The endpoint ID or UID |  |

### Return type

[**OperationalWebhookEndpointHeadersResponseDto**](OperationalWebhookEndpointHeadersResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="operationalwebhookcontrollergetsecret"></a>
# **OperationalWebhookControllerGetSecret**
> OperationalWebhookEndpointSecretResponseDto OperationalWebhookControllerGetSecret (string id)

Get Operational Webhook Endpoint Secret

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class OperationalWebhookControllerGetSecretExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new WebhookEndpointApi(config);
            var id = "id_example";  // string | The endpoint ID or UID

            try
            {
                // Get Operational Webhook Endpoint Secret
                OperationalWebhookEndpointSecretResponseDto result = apiInstance.OperationalWebhookControllerGetSecret(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEndpointApi.OperationalWebhookControllerGetSecret: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OperationalWebhookControllerGetSecretWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Operational Webhook Endpoint Secret
    ApiResponse<OperationalWebhookEndpointSecretResponseDto> response = apiInstance.OperationalWebhookControllerGetSecretWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEndpointApi.OperationalWebhookControllerGetSecretWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The endpoint ID or UID |  |

### Return type

[**OperationalWebhookEndpointSecretResponseDto**](OperationalWebhookEndpointSecretResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="operationalwebhookcontrollerlist"></a>
# **OperationalWebhookControllerList**
> OperationalWebhookEndpointListResponseDto OperationalWebhookControllerList ()

List Operational Webhook Endpoints

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class OperationalWebhookControllerListExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new WebhookEndpointApi(config);

            try
            {
                // List Operational Webhook Endpoints
                OperationalWebhookEndpointListResponseDto result = apiInstance.OperationalWebhookControllerList();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEndpointApi.OperationalWebhookControllerList: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OperationalWebhookControllerListWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Operational Webhook Endpoints
    ApiResponse<OperationalWebhookEndpointListResponseDto> response = apiInstance.OperationalWebhookControllerListWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEndpointApi.OperationalWebhookControllerListWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**OperationalWebhookEndpointListResponseDto**](OperationalWebhookEndpointListResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="operationalwebhookcontrollerrotatesecret"></a>
# **OperationalWebhookControllerRotateSecret**
> void OperationalWebhookControllerRotateSecret (string id, OperationalWebhookEndpointSecretInDto operationalWebhookEndpointSecretInDto)

Rotate Operational Webhook Endpoint Secret

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class OperationalWebhookControllerRotateSecretExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new WebhookEndpointApi(config);
            var id = "id_example";  // string | The endpoint ID or UID
            var operationalWebhookEndpointSecretInDto = new OperationalWebhookEndpointSecretInDto(); // OperationalWebhookEndpointSecretInDto | 

            try
            {
                // Rotate Operational Webhook Endpoint Secret
                apiInstance.OperationalWebhookControllerRotateSecret(id, operationalWebhookEndpointSecretInDto);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEndpointApi.OperationalWebhookControllerRotateSecret: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OperationalWebhookControllerRotateSecretWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Rotate Operational Webhook Endpoint Secret
    apiInstance.OperationalWebhookControllerRotateSecretWithHttpInfo(id, operationalWebhookEndpointSecretInDto);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEndpointApi.OperationalWebhookControllerRotateSecretWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The endpoint ID or UID |  |
| **operationalWebhookEndpointSecretInDto** | [**OperationalWebhookEndpointSecretInDto**](OperationalWebhookEndpointSecretInDto.md) |  |  |

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Secret rotated |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="operationalwebhookcontrollerupdate"></a>
# **OperationalWebhookControllerUpdate**
> OperationalWebhookEndpointResponseDto OperationalWebhookControllerUpdate (string id, OperationalWebhookEndpointUpdateDto operationalWebhookEndpointUpdateDto)

Update Operational Webhook Endpoint

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class OperationalWebhookControllerUpdateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new WebhookEndpointApi(config);
            var id = "id_example";  // string | The endpoint ID or UID
            var operationalWebhookEndpointUpdateDto = new OperationalWebhookEndpointUpdateDto(); // OperationalWebhookEndpointUpdateDto | 

            try
            {
                // Update Operational Webhook Endpoint
                OperationalWebhookEndpointResponseDto result = apiInstance.OperationalWebhookControllerUpdate(id, operationalWebhookEndpointUpdateDto);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEndpointApi.OperationalWebhookControllerUpdate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OperationalWebhookControllerUpdateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Operational Webhook Endpoint
    ApiResponse<OperationalWebhookEndpointResponseDto> response = apiInstance.OperationalWebhookControllerUpdateWithHttpInfo(id, operationalWebhookEndpointUpdateDto);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEndpointApi.OperationalWebhookControllerUpdateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The endpoint ID or UID |  |
| **operationalWebhookEndpointUpdateDto** | [**OperationalWebhookEndpointUpdateDto**](OperationalWebhookEndpointUpdateDto.md) |  |  |

### Return type

[**OperationalWebhookEndpointResponseDto**](OperationalWebhookEndpointResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="operationalwebhookcontrollerupdateheaders"></a>
# **OperationalWebhookControllerUpdateHeaders**
> void OperationalWebhookControllerUpdateHeaders (string id, OperationalWebhookEndpointHeadersInDto operationalWebhookEndpointHeadersInDto)

Set Operational Webhook Endpoint Headers

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class OperationalWebhookControllerUpdateHeadersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new WebhookEndpointApi(config);
            var id = "id_example";  // string | The endpoint ID or UID
            var operationalWebhookEndpointHeadersInDto = new OperationalWebhookEndpointHeadersInDto(); // OperationalWebhookEndpointHeadersInDto | 

            try
            {
                // Set Operational Webhook Endpoint Headers
                apiInstance.OperationalWebhookControllerUpdateHeaders(id, operationalWebhookEndpointHeadersInDto);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookEndpointApi.OperationalWebhookControllerUpdateHeaders: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OperationalWebhookControllerUpdateHeadersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Set Operational Webhook Endpoint Headers
    apiInstance.OperationalWebhookControllerUpdateHeadersWithHttpInfo(id, operationalWebhookEndpointHeadersInDto);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookEndpointApi.OperationalWebhookControllerUpdateHeadersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The endpoint ID or UID |  |
| **operationalWebhookEndpointHeadersInDto** | [**OperationalWebhookEndpointHeadersInDto**](OperationalWebhookEndpointHeadersInDto.md) |  |  |

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Headers set |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

