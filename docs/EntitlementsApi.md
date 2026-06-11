# Solifyn.Api.EntitlementsApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**EntitlementsCreate**](EntitlementsApi.md#entitlementscreate) | **POST** /v1/entitlements | Create Entitlement |
| [**EntitlementsDelete**](EntitlementsApi.md#entitlementsdelete) | **DELETE** /v1/entitlements/{id} | Delete Entitlement |
| [**EntitlementsGet**](EntitlementsApi.md#entitlementsget) | **GET** /v1/entitlements/{id} | Retrieve Entitlement |
| [**EntitlementsList**](EntitlementsApi.md#entitlementslist) | **GET** /v1/entitlements | List Entitlements |
| [**EntitlementsUpdate**](EntitlementsApi.md#entitlementsupdate) | **PATCH** /v1/entitlements/{id} | Update Entitlement |

<a id="entitlementscreate"></a>
# **EntitlementsCreate**
> EntitlementDetailResponseDto EntitlementsCreate (CreateEntitlementDto createEntitlementDto)

Create Entitlement

Create a new independent access entitlement.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class EntitlementsCreateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            var apiInstance = new EntitlementsApi(config);
            var createEntitlementDto = new CreateEntitlementDto(); // CreateEntitlementDto | 

            try
            {
                // Create Entitlement
                EntitlementDetailResponseDto result = apiInstance.EntitlementsCreate(createEntitlementDto);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EntitlementsApi.EntitlementsCreate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EntitlementsCreateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Entitlement
    ApiResponse<EntitlementDetailResponseDto> response = apiInstance.EntitlementsCreateWithHttpInfo(createEntitlementDto);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EntitlementsApi.EntitlementsCreateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createEntitlementDto** | [**CreateEntitlementDto**](CreateEntitlementDto.md) |  |  |

### Return type

[**EntitlementDetailResponseDto**](EntitlementDetailResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Entitlement created successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="entitlementsdelete"></a>
# **EntitlementsDelete**
> EntitlementDetailResponseDto EntitlementsDelete (string id)

Delete Entitlement

Delete an independent entitlement and unlink all mapped products.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class EntitlementsDeleteExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            var apiInstance = new EntitlementsApi(config);
            var id = ent_8Z1aB2cD3eF4gH5iJ6kL7m;  // string | The unique entitlement ID.

            try
            {
                // Delete Entitlement
                EntitlementDetailResponseDto result = apiInstance.EntitlementsDelete(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EntitlementsApi.EntitlementsDelete: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EntitlementsDeleteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete Entitlement
    ApiResponse<EntitlementDetailResponseDto> response = apiInstance.EntitlementsDeleteWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EntitlementsApi.EntitlementsDeleteWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The unique entitlement ID. |  |

### Return type

[**EntitlementDetailResponseDto**](EntitlementDetailResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Entitlement deleted successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="entitlementsget"></a>
# **EntitlementsGet**
> EntitlementDetailResponseDto EntitlementsGet (string id)

Retrieve Entitlement

Retrieve a specific entitlement definition by ID.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class EntitlementsGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            var apiInstance = new EntitlementsApi(config);
            var id = ent_8Z1aB2cD3eF4gH5iJ6kL7m;  // string | The unique entitlement ID.

            try
            {
                // Retrieve Entitlement
                EntitlementDetailResponseDto result = apiInstance.EntitlementsGet(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EntitlementsApi.EntitlementsGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EntitlementsGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieve Entitlement
    ApiResponse<EntitlementDetailResponseDto> response = apiInstance.EntitlementsGetWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EntitlementsApi.EntitlementsGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The unique entitlement ID. |  |

### Return type

[**EntitlementDetailResponseDto**](EntitlementDetailResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Entitlement retrieved successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="entitlementslist"></a>
# **EntitlementsList**
> List&lt;EntitlementDetailResponseDto&gt; EntitlementsList ()

List Entitlements

List all independent entitlements for the active business.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class EntitlementsListExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            var apiInstance = new EntitlementsApi(config);

            try
            {
                // List Entitlements
                List<EntitlementDetailResponseDto> result = apiInstance.EntitlementsList();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EntitlementsApi.EntitlementsList: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EntitlementsListWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Entitlements
    ApiResponse<List<EntitlementDetailResponseDto>> response = apiInstance.EntitlementsListWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EntitlementsApi.EntitlementsListWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**List&lt;EntitlementDetailResponseDto&gt;**](EntitlementDetailResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Entitlements retrieved successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="entitlementsupdate"></a>
# **EntitlementsUpdate**
> EntitlementDetailResponseDto EntitlementsUpdate (string id, UpdateEntitlementDto updateEntitlementDto)

Update Entitlement

Update details of an existing independent entitlement.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class EntitlementsUpdateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            var apiInstance = new EntitlementsApi(config);
            var id = ent_8Z1aB2cD3eF4gH5iJ6kL7m;  // string | The unique entitlement ID.
            var updateEntitlementDto = new UpdateEntitlementDto(); // UpdateEntitlementDto | 

            try
            {
                // Update Entitlement
                EntitlementDetailResponseDto result = apiInstance.EntitlementsUpdate(id, updateEntitlementDto);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EntitlementsApi.EntitlementsUpdate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EntitlementsUpdateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Entitlement
    ApiResponse<EntitlementDetailResponseDto> response = apiInstance.EntitlementsUpdateWithHttpInfo(id, updateEntitlementDto);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EntitlementsApi.EntitlementsUpdateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The unique entitlement ID. |  |
| **updateEntitlementDto** | [**UpdateEntitlementDto**](UpdateEntitlementDto.md) |  |  |

### Return type

[**EntitlementDetailResponseDto**](EntitlementDetailResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Entitlement updated successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

