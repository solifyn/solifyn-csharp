# Solifyn.Api.LicenseKeysClientApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**LicensesActivate**](LicenseKeysClientApi.md#licensesactivate) | **POST** /v1/licenses/activate | Activate License Key |
| [**LicensesDeactivate**](LicenseKeysClientApi.md#licensesdeactivate) | **POST** /v1/licenses/deactivate/{instanceId} | Deactivate Instance |
| [**LicensesInstances**](LicenseKeysClientApi.md#licensesinstances) | **GET** /v1/licenses/instances/{licenseId} | Get Active Instances |
| [**LicensesVerify**](LicenseKeysClientApi.md#licensesverify) | **POST** /v1/licenses/verify | Validate License Key |

<a id="licensesactivate"></a>
# **LicensesActivate**
> Instance LicensesActivate (LicensesActivateRequest licensesActivateRequest)

Activate License Key

Register and activate a device or instance for a specific license key.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class LicensesActivateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new LicenseKeysClientApi(config);
            var licensesActivateRequest = new LicensesActivateRequest(); // LicensesActivateRequest | 

            try
            {
                // Activate License Key
                Instance result = apiInstance.LicensesActivate(licensesActivateRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LicenseKeysClientApi.LicensesActivate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LicensesActivateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Activate License Key
    ApiResponse<Instance> response = apiInstance.LicensesActivateWithHttpInfo(licensesActivateRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LicenseKeysClientApi.LicensesActivateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **licensesActivateRequest** | [**LicensesActivateRequest**](LicensesActivateRequest.md) |  |  |

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
| **200** | Activation successful. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="licensesdeactivate"></a>
# **LicensesDeactivate**
> LicensesDeactivate200Response LicensesDeactivate (Guid instanceId, LicensesDeactivateRequest licensesDeactivateRequest)

Deactivate Instance

Deactivate or unregister an active device instance from a license key.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class LicensesDeactivateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new LicenseKeysClientApi(config);
            var instanceId = "instanceId_example";  // Guid | The unique device instance ID.
            var licensesDeactivateRequest = new LicensesDeactivateRequest(); // LicensesDeactivateRequest | 

            try
            {
                // Deactivate Instance
                LicensesDeactivate200Response result = apiInstance.LicensesDeactivate(instanceId, licensesDeactivateRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LicenseKeysClientApi.LicensesDeactivate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LicensesDeactivateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Deactivate Instance
    ApiResponse<LicensesDeactivate200Response> response = apiInstance.LicensesDeactivateWithHttpInfo(instanceId, licensesDeactivateRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LicenseKeysClientApi.LicensesDeactivateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **instanceId** | **Guid** | The unique device instance ID. |  |
| **licensesDeactivateRequest** | [**LicensesDeactivateRequest**](LicensesDeactivateRequest.md) |  |  |

### Return type

[**LicensesDeactivate200Response**](LicensesDeactivate200Response.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Instance deactivated successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="licensesinstances"></a>
# **LicensesInstances**
> List&lt;Instance&gt; LicensesInstances (Guid licenseId)

Get Active Instances

List all active devices or server instances linked to a specific license key.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class LicensesInstancesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new LicenseKeysClientApi(config);
            var licenseId = "licenseId_example";  // Guid | The unique license key ID.

            try
            {
                // Get Active Instances
                List<Instance> result = apiInstance.LicensesInstances(licenseId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LicenseKeysClientApi.LicensesInstances: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LicensesInstancesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Active Instances
    ApiResponse<List<Instance>> response = apiInstance.LicensesInstancesWithHttpInfo(licenseId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LicenseKeysClientApi.LicensesInstancesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **licenseId** | **Guid** | The unique license key ID. |  |

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
| **200** | Successfully retrieved active instances. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="licensesverify"></a>
# **LicensesVerify**
> LicenseValidationResponse LicensesVerify (LicensesVerifyRequest licensesVerifyRequest)

Validate License Key

Verify if a software license key is valid, active, and has not exceeded its limits.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class LicensesVerifyExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new LicenseKeysClientApi(config);
            var licensesVerifyRequest = new LicensesVerifyRequest(); // LicensesVerifyRequest | 

            try
            {
                // Validate License Key
                LicenseValidationResponse result = apiInstance.LicensesVerify(licensesVerifyRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LicenseKeysClientApi.LicensesVerify: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LicensesVerifyWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Validate License Key
    ApiResponse<LicenseValidationResponse> response = apiInstance.LicensesVerifyWithHttpInfo(licensesVerifyRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LicenseKeysClientApi.LicensesVerifyWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **licensesVerifyRequest** | [**LicensesVerifyRequest**](LicensesVerifyRequest.md) |  |  |

### Return type

[**LicenseValidationResponse**](LicenseValidationResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | License is valid. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

