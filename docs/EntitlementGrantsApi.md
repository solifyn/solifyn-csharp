# Solifyn.Api.EntitlementGrantsApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**EntitlementGrantsGet**](EntitlementGrantsApi.md#entitlementgrantsget) | **GET** /v1/entitlement-grants/{id} | Retrieve Entitlement Grant |
| [**EntitlementGrantsList**](EntitlementGrantsApi.md#entitlementgrantslist) | **GET** /v1/entitlement-grants | List Entitlement Grants |
| [**EntitlementGrantsRetry**](EntitlementGrantsApi.md#entitlementgrantsretry) | **POST** /v1/entitlement-grants/{id}/retry | Retry Entitlement Grant Delivery |
| [**EntitlementGrantsRevoke**](EntitlementGrantsApi.md#entitlementgrantsrevoke) | **POST** /v1/entitlement-grants/{id}/revoke | Manually Revoke Entitlement Grant |

<a id="entitlementgrantsget"></a>
# **EntitlementGrantsGet**
> EntitlementGrantResponseDto EntitlementGrantsGet (string id)

Retrieve Entitlement Grant

Retrieve details of a specific entitlement grant.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class EntitlementGrantsGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new EntitlementGrantsApi(config);
            var id = "id_example";  // string | The unique grant ID

            try
            {
                // Retrieve Entitlement Grant
                EntitlementGrantResponseDto result = apiInstance.EntitlementGrantsGet(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EntitlementGrantsApi.EntitlementGrantsGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EntitlementGrantsGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieve Entitlement Grant
    ApiResponse<EntitlementGrantResponseDto> response = apiInstance.EntitlementGrantsGetWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EntitlementGrantsApi.EntitlementGrantsGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The unique grant ID |  |

### Return type

[**EntitlementGrantResponseDto**](EntitlementGrantResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Details of the grant. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="entitlementgrantslist"></a>
# **EntitlementGrantsList**
> List&lt;EntitlementGrantResponseDto&gt; EntitlementGrantsList (string status = null, string entitlementId = null, string productId = null)

List Entitlement Grants

Retrieve all GitHub repository entitlement grants for the active business.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class EntitlementGrantsListExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new EntitlementGrantsApi(config);
            var status = "status_example";  // string | Filter by status (PENDING, DELIVERED, FAILED, REVOKED) (optional) 
            var entitlementId = "entitlementId_example";  // string | Filter by entitlement config ID (optional) 
            var productId = "productId_example";  // string | Filter by product ID (optional) 

            try
            {
                // List Entitlement Grants
                List<EntitlementGrantResponseDto> result = apiInstance.EntitlementGrantsList(status, entitlementId, productId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EntitlementGrantsApi.EntitlementGrantsList: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EntitlementGrantsListWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Entitlement Grants
    ApiResponse<List<EntitlementGrantResponseDto>> response = apiInstance.EntitlementGrantsListWithHttpInfo(status, entitlementId, productId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EntitlementGrantsApi.EntitlementGrantsListWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **status** | **string** | Filter by status (PENDING, DELIVERED, FAILED, REVOKED) | [optional]  |
| **entitlementId** | **string** | Filter by entitlement config ID | [optional]  |
| **productId** | **string** | Filter by product ID | [optional]  |

### Return type

[**List&lt;EntitlementGrantResponseDto&gt;**](EntitlementGrantResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved list of grants. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="entitlementgrantsretry"></a>
# **EntitlementGrantsRetry**
> EntitlementGrantResponseDto EntitlementGrantsRetry (string id)

Retry Entitlement Grant Delivery

Attempts to re-invite the collaborator if GitHub username is already connected, or resets the OAuth URL redirect.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class EntitlementGrantsRetryExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new EntitlementGrantsApi(config);
            var id = "id_example";  // string | The unique grant ID

            try
            {
                // Retry Entitlement Grant Delivery
                EntitlementGrantResponseDto result = apiInstance.EntitlementGrantsRetry(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EntitlementGrantsApi.EntitlementGrantsRetry: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EntitlementGrantsRetryWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retry Entitlement Grant Delivery
    ApiResponse<EntitlementGrantResponseDto> response = apiInstance.EntitlementGrantsRetryWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EntitlementGrantsApi.EntitlementGrantsRetryWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The unique grant ID |  |

### Return type

[**EntitlementGrantResponseDto**](EntitlementGrantResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Grant delivery retried. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="entitlementgrantsrevoke"></a>
# **EntitlementGrantsRevoke**
> EntitlementGrantResponseDto EntitlementGrantsRevoke (string id)

Manually Revoke Entitlement Grant

Manually remove the customer collaborator access from the repository and revoke the grant.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class EntitlementGrantsRevokeExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new EntitlementGrantsApi(config);
            var id = "id_example";  // string | The unique grant ID

            try
            {
                // Manually Revoke Entitlement Grant
                EntitlementGrantResponseDto result = apiInstance.EntitlementGrantsRevoke(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EntitlementGrantsApi.EntitlementGrantsRevoke: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EntitlementGrantsRevokeWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Manually Revoke Entitlement Grant
    ApiResponse<EntitlementGrantResponseDto> response = apiInstance.EntitlementGrantsRevokeWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EntitlementGrantsApi.EntitlementGrantsRevokeWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The unique grant ID |  |

### Return type

[**EntitlementGrantResponseDto**](EntitlementGrantResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Grant successfully revoked. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

