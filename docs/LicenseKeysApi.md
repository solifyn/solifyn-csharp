# Solifyn.Api.LicenseKeysApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**LicensesCreate**](LicenseKeysApi.md#licensescreate) | **POST** /v1/licenses | Create License Key |
| [**LicensesDeleteInstance**](LicenseKeysApi.md#licensesdeleteinstance) | **DELETE** /v1/licenses/instances/{instanceId} | Force Delete Instance |
| [**LicensesGet**](LicenseKeysApi.md#licensesget) | **GET** /v1/licenses/{id} | Get License Key |
| [**LicensesGetInstance**](LicenseKeysApi.md#licensesgetinstance) | **GET** /v1/licenses/{id}/instances/{instanceId} | Get License Key Instance |
| [**LicensesGetInstances**](LicenseKeysApi.md#licensesgetinstances) | **GET** /v1/licenses/{id}/instances | Get License Key Instances |
| [**LicensesList**](LicenseKeysApi.md#licenseslist) | **GET** /v1/licenses | List License Keys |
| [**LicensesToggle**](LicenseKeysApi.md#licensestoggle) | **POST** /v1/licenses/{id}/toggle | Toggle License Status |
| [**LicensesUpdate**](LicenseKeysApi.md#licensesupdate) | **PATCH** /v1/licenses/{id} | Update License Key |
| [**LicensesUpdateInstance**](LicenseKeysApi.md#licensesupdateinstance) | **PATCH** /v1/licenses/{id}/instances/{instanceId} | Update License Key Instance |
| [**LicensesUpdateInstancePost**](LicenseKeysApi.md#licensesupdateinstancepost) | **POST** /v1/licenses/{id}/instances/{instanceId} | Update License Key Instance (POST) |

<a id="licensescreate"></a>
# **LicensesCreate**
> License LicensesCreate (LicensesCreateRequest licensesCreateRequest)

Create License Key

Manually issue a new license key for a specific product.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class LicensesCreateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new LicenseKeysApi(config);
            var licensesCreateRequest = new LicensesCreateRequest(); // LicensesCreateRequest | 

            try
            {
                // Create License Key
                License result = apiInstance.LicensesCreate(licensesCreateRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LicenseKeysApi.LicensesCreate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LicensesCreateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create License Key
    ApiResponse<License> response = apiInstance.LicensesCreateWithHttpInfo(licensesCreateRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LicenseKeysApi.LicensesCreateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **licensesCreateRequest** | [**LicensesCreateRequest**](LicensesCreateRequest.md) |  |  |

### Return type

[**License**](License.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully created license. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="licensesdeleteinstance"></a>
# **LicensesDeleteInstance**
> Instance LicensesDeleteInstance (string instanceId)

Force Delete Instance

Administrative endpoint to force-delete an instance globally by its database ID.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class LicensesDeleteInstanceExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new LicenseKeysApi(config);
            var instanceId = inc_123;  // string | The unique hardware activation instance ID.

            try
            {
                // Force Delete Instance
                Instance result = apiInstance.LicensesDeleteInstance(instanceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LicenseKeysApi.LicensesDeleteInstance: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LicensesDeleteInstanceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Force Delete Instance
    ApiResponse<Instance> response = apiInstance.LicensesDeleteInstanceWithHttpInfo(instanceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LicenseKeysApi.LicensesDeleteInstanceWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **instanceId** | **string** | The unique hardware activation instance ID. |  |

### Return type

[**Instance**](Instance.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Instance deactivated/deleted successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="licensesget"></a>
# **LicensesGet**
> License LicensesGet (Guid id)

Get License Key

Retrieve complete administrative details of a specific license key.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class LicensesGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new LicenseKeysApi(config);
            var id = "id_example";  // Guid | The unique license key ID.

            try
            {
                // Get License Key
                License result = apiInstance.LicensesGet(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LicenseKeysApi.LicensesGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LicensesGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get License Key
    ApiResponse<License> response = apiInstance.LicensesGetWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LicenseKeysApi.LicensesGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **Guid** | The unique license key ID. |  |

### Return type

[**License**](License.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved license details. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="licensesgetinstance"></a>
# **LicensesGetInstance**
> Instance LicensesGetInstance (Guid id, string instanceId)

Get License Key Instance

Retrieve administrative details of a specific software license instance.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class LicensesGetInstanceExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new LicenseKeysApi(config);
            var id = "id_example";  // Guid | The unique administrative identifier (ID) of the parent license key.
            var instanceId = inc_123;  // string | The client-generated instance ID (hardware hash) or the internal database ID of the instance.

            try
            {
                // Get License Key Instance
                Instance result = apiInstance.LicensesGetInstance(id, instanceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LicenseKeysApi.LicensesGetInstance: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LicensesGetInstanceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get License Key Instance
    ApiResponse<Instance> response = apiInstance.LicensesGetInstanceWithHttpInfo(id, instanceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LicenseKeysApi.LicensesGetInstanceWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **Guid** | The unique administrative identifier (ID) of the parent license key. |  |
| **instanceId** | **string** | The client-generated instance ID (hardware hash) or the internal database ID of the instance. |  |

### Return type

[**Instance**](Instance.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved instance. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="licensesgetinstances"></a>
# **LicensesGetInstances**
> List&lt;Instance&gt; LicensesGetInstances (string id)

Get License Key Instances

Retrieve all active devices/instances for a specific administrative license key.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class LicensesGetInstancesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new LicenseKeysApi(config);
            var id = lic_123;  // string | The unique administrative identifier (ID) of the parent license key.

            try
            {
                // Get License Key Instances
                List<Instance> result = apiInstance.LicensesGetInstances(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LicenseKeysApi.LicensesGetInstances: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LicensesGetInstancesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get License Key Instances
    ApiResponse<List<Instance>> response = apiInstance.LicensesGetInstancesWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LicenseKeysApi.LicensesGetInstancesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The unique administrative identifier (ID) of the parent license key. |  |

### Return type

[**List&lt;Instance&gt;**](Instance.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved instances. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="licenseslist"></a>
# **LicensesList**
> List&lt;License&gt; LicensesList ()

List License Keys

List all administrative license keys belonging to products under your active business.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class LicensesListExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new LicenseKeysApi(config);

            try
            {
                // List License Keys
                List<License> result = apiInstance.LicensesList();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LicenseKeysApi.LicensesList: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LicensesListWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List License Keys
    ApiResponse<List<License>> response = apiInstance.LicensesListWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LicenseKeysApi.LicensesListWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**List&lt;License&gt;**](License.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved licenses list. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="licensestoggle"></a>
# **LicensesToggle**
> License LicensesToggle (string id)

Toggle License Status

Toggle the status of a specific license key between ACTIVE and DISABLED.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class LicensesToggleExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new LicenseKeysApi(config);
            var id = lic_123;  // string | The unique license key ID.

            try
            {
                // Toggle License Status
                License result = apiInstance.LicensesToggle(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LicenseKeysApi.LicensesToggle: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LicensesToggleWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Toggle License Status
    ApiResponse<License> response = apiInstance.LicensesToggleWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LicenseKeysApi.LicensesToggleWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The unique license key ID. |  |

### Return type

[**License**](License.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Status toggled successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="licensesupdate"></a>
# **LicensesUpdate**
> License LicensesUpdate (Guid id, LicensesUpdateRequest licensesUpdateRequest)

Update License Key

Update limits or status of an existing license key.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class LicensesUpdateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new LicenseKeysApi(config);
            var id = "id_example";  // Guid | The unique license key ID.
            var licensesUpdateRequest = new LicensesUpdateRequest(); // LicensesUpdateRequest | 

            try
            {
                // Update License Key
                License result = apiInstance.LicensesUpdate(id, licensesUpdateRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LicenseKeysApi.LicensesUpdate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LicensesUpdateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update License Key
    ApiResponse<License> response = apiInstance.LicensesUpdateWithHttpInfo(id, licensesUpdateRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LicenseKeysApi.LicensesUpdateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **Guid** | The unique license key ID. |  |
| **licensesUpdateRequest** | [**LicensesUpdateRequest**](LicensesUpdateRequest.md) |  |  |

### Return type

[**License**](License.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully updated license. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="licensesupdateinstance"></a>
# **LicensesUpdateInstance**
> Instance LicensesUpdateInstance (string instanceId, Guid id, LicensesUpdateInstancePostRequest licensesUpdateInstancePostRequest)

Update License Key Instance

Update administrative details (like friendly display name or custom IP) of an active license device instance.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class LicensesUpdateInstanceExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new LicenseKeysApi(config);
            var instanceId = inc_123;  // string | The client-generated instance ID (hardware hash) or the internal database ID of the instance.
            var id = "id_example";  // Guid | The unique administrative identifier (ID) of the parent license key.
            var licensesUpdateInstancePostRequest = new LicensesUpdateInstancePostRequest(); // LicensesUpdateInstancePostRequest | 

            try
            {
                // Update License Key Instance
                Instance result = apiInstance.LicensesUpdateInstance(instanceId, id, licensesUpdateInstancePostRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LicenseKeysApi.LicensesUpdateInstance: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LicensesUpdateInstanceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update License Key Instance
    ApiResponse<Instance> response = apiInstance.LicensesUpdateInstanceWithHttpInfo(instanceId, id, licensesUpdateInstancePostRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LicenseKeysApi.LicensesUpdateInstanceWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **instanceId** | **string** | The client-generated instance ID (hardware hash) or the internal database ID of the instance. |  |
| **id** | **Guid** | The unique administrative identifier (ID) of the parent license key. |  |
| **licensesUpdateInstancePostRequest** | [**LicensesUpdateInstancePostRequest**](LicensesUpdateInstancePostRequest.md) |  |  |

### Return type

[**Instance**](Instance.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully updated instance. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="licensesupdateinstancepost"></a>
# **LicensesUpdateInstancePost**
> Instance LicensesUpdateInstancePost (string instanceId, Guid id, LicensesUpdateInstancePostRequest licensesUpdateInstancePostRequest)

Update License Key Instance (POST)

Alternative POST endpoint to update administrative details (like friendly display name or custom IP) of an active license device instance.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class LicensesUpdateInstancePostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new LicenseKeysApi(config);
            var instanceId = inc_123;  // string | The client-generated instance ID (hardware hash) or the internal database ID of the instance.
            var id = "id_example";  // Guid | The unique administrative identifier (ID) of the parent license key.
            var licensesUpdateInstancePostRequest = new LicensesUpdateInstancePostRequest(); // LicensesUpdateInstancePostRequest | 

            try
            {
                // Update License Key Instance (POST)
                Instance result = apiInstance.LicensesUpdateInstancePost(instanceId, id, licensesUpdateInstancePostRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LicenseKeysApi.LicensesUpdateInstancePost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LicensesUpdateInstancePostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update License Key Instance (POST)
    ApiResponse<Instance> response = apiInstance.LicensesUpdateInstancePostWithHttpInfo(instanceId, id, licensesUpdateInstancePostRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LicenseKeysApi.LicensesUpdateInstancePostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **instanceId** | **string** | The client-generated instance ID (hardware hash) or the internal database ID of the instance. |  |
| **id** | **Guid** | The unique administrative identifier (ID) of the parent license key. |  |
| **licensesUpdateInstancePostRequest** | [**LicensesUpdateInstancePostRequest**](LicensesUpdateInstancePostRequest.md) |  |  |

### Return type

[**Instance**](Instance.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully updated instance. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

