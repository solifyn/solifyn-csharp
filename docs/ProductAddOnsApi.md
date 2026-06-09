# Solifyn.Api.ProductAddOnsApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ProductsCreateAddon**](ProductAddOnsApi.md#productscreateaddon) | **POST** /v1/products/{id}/addons | Create Product Add-on |
| [**ProductsDeleteAddon**](ProductAddOnsApi.md#productsdeleteaddon) | **DELETE** /v1/products/{id}/addons/{addonId} | Delete Product Add-on |
| [**ProductsGetAddon**](ProductAddOnsApi.md#productsgetaddon) | **GET** /v1/products/{id}/addons/{addonId} | Retrieve Product Add-on |
| [**ProductsListAddons**](ProductAddOnsApi.md#productslistaddons) | **GET** /v1/products/{id}/addons | List Product Add-ons |
| [**ProductsListAllAddons**](ProductAddOnsApi.md#productslistalladdons) | **GET** /v1/products/all-addons/list | List All Add-ons |
| [**ProductsUpdateAddon**](ProductAddOnsApi.md#productsupdateaddon) | **PATCH** /v1/products/{id}/addons/{addonId} | Update Product Add-on |

<a id="productscreateaddon"></a>
# **ProductsCreateAddon**
> Addon ProductsCreateAddon (string id, AddonCreate addonCreate)

Create Product Add-on

Attach a new add-on configuration to a product.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class ProductsCreateAddonExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new ProductAddOnsApi(config);
            var id = prod_parent_123;  // string | The parent product ID.
            var addonCreate = new AddonCreate(); // AddonCreate | 

            try
            {
                // Create Product Add-on
                Addon result = apiInstance.ProductsCreateAddon(id, addonCreate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductAddOnsApi.ProductsCreateAddon: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ProductsCreateAddonWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Product Add-on
    ApiResponse<Addon> response = apiInstance.ProductsCreateAddonWithHttpInfo(id, addonCreate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductAddOnsApi.ProductsCreateAddonWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The parent product ID. |  |
| **addonCreate** | [**AddonCreate**](AddonCreate.md) |  |  |

### Return type

[**Addon**](Addon.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Add-on attached successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="productsdeleteaddon"></a>
# **ProductsDeleteAddon**
> ProductMessageResponseDto ProductsDeleteAddon (string id, string addonId)

Delete Product Add-on

Remove an add-on configuration from a product.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class ProductsDeleteAddonExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new ProductAddOnsApi(config);
            var id = prod_parent_123;  // string | The parent product ID.
            var addonId = prod_addon_123;  // string | The add-on product ID to remove.

            try
            {
                // Delete Product Add-on
                ProductMessageResponseDto result = apiInstance.ProductsDeleteAddon(id, addonId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductAddOnsApi.ProductsDeleteAddon: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ProductsDeleteAddonWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete Product Add-on
    ApiResponse<ProductMessageResponseDto> response = apiInstance.ProductsDeleteAddonWithHttpInfo(id, addonId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductAddOnsApi.ProductsDeleteAddonWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The parent product ID. |  |
| **addonId** | **string** | The add-on product ID to remove. |  |

### Return type

[**ProductMessageResponseDto**](ProductMessageResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Add-on configuration removed successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="productsgetaddon"></a>
# **ProductsGetAddon**
> Addon ProductsGetAddon (string id, string addonId)

Retrieve Product Add-on

Retrieve a specific add-on configuration of a product.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class ProductsGetAddonExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new ProductAddOnsApi(config);
            var id = prod_parent_123;  // string | The parent product ID.
            var addonId = prod_addon_123;  // string | The add-on product ID.

            try
            {
                // Retrieve Product Add-on
                Addon result = apiInstance.ProductsGetAddon(id, addonId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductAddOnsApi.ProductsGetAddon: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ProductsGetAddonWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieve Product Add-on
    ApiResponse<Addon> response = apiInstance.ProductsGetAddonWithHttpInfo(id, addonId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductAddOnsApi.ProductsGetAddonWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The parent product ID. |  |
| **addonId** | **string** | The add-on product ID. |  |

### Return type

[**Addon**](Addon.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved add-on configuration. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="productslistaddons"></a>
# **ProductsListAddons**
> List&lt;Addon&gt; ProductsListAddons (string id)

List Product Add-ons

Retrieve all add-on configurations attached to a product.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class ProductsListAddonsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new ProductAddOnsApi(config);
            var id = prod_parent_123;  // string | The parent product ID.

            try
            {
                // List Product Add-ons
                List<Addon> result = apiInstance.ProductsListAddons(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductAddOnsApi.ProductsListAddons: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ProductsListAddonsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Product Add-ons
    ApiResponse<List<Addon>> response = apiInstance.ProductsListAddonsWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductAddOnsApi.ProductsListAddonsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The parent product ID. |  |

### Return type

[**List&lt;Addon&gt;**](Addon.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | List of product add-on configurations. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="productslistalladdons"></a>
# **ProductsListAllAddons**
> void ProductsListAllAddons ()

List All Add-ons

Retrieve all configured add-on configurations for the active business.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class ProductsListAllAddonsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new ProductAddOnsApi(config);

            try
            {
                // List All Add-ons
                apiInstance.ProductsListAllAddons();
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductAddOnsApi.ProductsListAllAddons: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ProductsListAllAddonsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List All Add-ons
    apiInstance.ProductsListAllAddonsWithHttpInfo();
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductAddOnsApi.ProductsListAllAddonsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
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
| **200** | Successfully retrieved list of all addons. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="productsupdateaddon"></a>
# **ProductsUpdateAddon**
> Addon ProductsUpdateAddon (string id, string addonId, AddonUpdate addonUpdate)

Update Product Add-on

Update an existing add-on configuration for a product.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class ProductsUpdateAddonExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new ProductAddOnsApi(config);
            var id = prod_parent_123;  // string | The parent product ID.
            var addonId = prod_addon_123;  // string | The add-on product ID.
            var addonUpdate = new AddonUpdate(); // AddonUpdate | 

            try
            {
                // Update Product Add-on
                Addon result = apiInstance.ProductsUpdateAddon(id, addonId, addonUpdate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductAddOnsApi.ProductsUpdateAddon: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ProductsUpdateAddonWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Product Add-on
    ApiResponse<Addon> response = apiInstance.ProductsUpdateAddonWithHttpInfo(id, addonId, addonUpdate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductAddOnsApi.ProductsUpdateAddonWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The parent product ID. |  |
| **addonId** | **string** | The add-on product ID. |  |
| **addonUpdate** | [**AddonUpdate**](AddonUpdate.md) |  |  |

### Return type

[**Addon**](Addon.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Add-on configuration updated successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

