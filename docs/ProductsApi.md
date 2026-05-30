# Solifyn.Api.ProductsApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ProductsArchive**](ProductsApi.md#productsarchive) | **DELETE** /v1/products/{id} | Archive Product |
| [**ProductsCreate**](ProductsApi.md#productscreate) | **POST** /v1/products | Create Product |
| [**ProductsGet**](ProductsApi.md#productsget) | **GET** /v1/products/{id} | Retrieve Product |
| [**ProductsList**](ProductsApi.md#productslist) | **GET** /v1/products | List Products |
| [**ProductsUnarchive**](ProductsApi.md#productsunarchive) | **POST** /v1/products/{id}/unarchive | Unarchive Product |
| [**ProductsUpdate**](ProductsApi.md#productsupdate) | **PATCH** /v1/products/{id} | Update Product |

<a id="productsarchive"></a>
# **ProductsArchive**
> ProductsArchive200Response ProductsArchive (string id)

Archive Product

Archive a specific product to hide it from checkout pages and search results. Products are soft-deleted (archived) and can be restored using the unarchive endpoint.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class ProductsArchiveExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new ProductsApi(config);
            var id = prod_123;  // string | The unique product ID to archive.

            try
            {
                // Archive Product
                ProductsArchive200Response result = apiInstance.ProductsArchive(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductsApi.ProductsArchive: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ProductsArchiveWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Archive Product
    ApiResponse<ProductsArchive200Response> response = apiInstance.ProductsArchiveWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductsApi.ProductsArchiveWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The unique product ID to archive. |  |

### Return type

[**ProductsArchive200Response**](ProductsArchive200Response.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Product archived successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="productscreate"></a>
# **ProductsCreate**
> Product ProductsCreate (ProductCreate productCreate)

Create Product

Create a new product within your active business.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class ProductsCreateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new ProductsApi(config);
            var productCreate = new ProductCreate(); // ProductCreate | 

            try
            {
                // Create Product
                Product result = apiInstance.ProductsCreate(productCreate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductsApi.ProductsCreate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ProductsCreateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Product
    ApiResponse<Product> response = apiInstance.ProductsCreateWithHttpInfo(productCreate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductsApi.ProductsCreateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **productCreate** | [**ProductCreate**](ProductCreate.md) |  |  |

### Return type

[**Product**](Product.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Product created successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="productsget"></a>
# **ProductsGet**
> Product ProductsGet (string id)

Retrieve Product

Retrieve details of a specific product using its ID.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class ProductsGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new ProductsApi(config);
            var id = prod_123;  // string | The unique product ID.

            try
            {
                // Retrieve Product
                Product result = apiInstance.ProductsGet(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductsApi.ProductsGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ProductsGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieve Product
    ApiResponse<Product> response = apiInstance.ProductsGetWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductsApi.ProductsGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The unique product ID. |  |

### Return type

[**Product**](Product.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved product details. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="productslist"></a>
# **ProductsList**
> ProductsList200Response ProductsList (string pricingType = null, string sorting = null, decimal? limit = null, decimal? page = null, bool? isRecurring = null, bool? isArchived = null, string query = null, string id = null)

List Products

List and query products belonging to your active business with support for fuzzy search, filters, pagination, and sorting.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class ProductsListExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new ProductsApi(config);
            var pricingType = "pricingType_example";  // string | Filter by pricing type. (optional) 
            var sorting = "created_at";  // string | Sorting criterion. Add a minus sign - before the criteria name to sort by descending order. (optional) 
            var limit = 10MD;  // decimal? | Size of a page, defaults to 10. Maximum is 100. (optional)  (default to 10M)
            var page = 1MD;  // decimal? | Page number, defaults to 1. (optional)  (default to 1M)
            var isRecurring = true;  // bool? | Filter on recurring products (subscriptions). If true, only subscription tiers are returned. If false, only one-time purchase products are returned. (optional) 
            var isArchived = true;  // bool? | Filter by archived status. (optional) 
            var query = "query_example";  // string | Filter by product name (fuzzy, case-insensitive). (optional) 
            var id = "id_example";  // string | Filter by product ID. (optional) 

            try
            {
                // List Products
                ProductsList200Response result = apiInstance.ProductsList(pricingType, sorting, limit, page, isRecurring, isArchived, query, id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductsApi.ProductsList: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ProductsListWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Products
    ApiResponse<ProductsList200Response> response = apiInstance.ProductsListWithHttpInfo(pricingType, sorting, limit, page, isRecurring, isArchived, query, id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductsApi.ProductsListWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **pricingType** | **string** | Filter by pricing type. | [optional]  |
| **sorting** | **string** | Sorting criterion. Add a minus sign - before the criteria name to sort by descending order. | [optional]  |
| **limit** | **decimal?** | Size of a page, defaults to 10. Maximum is 100. | [optional] [default to 10M] |
| **page** | **decimal?** | Page number, defaults to 1. | [optional] [default to 1M] |
| **isRecurring** | **bool?** | Filter on recurring products (subscriptions). If true, only subscription tiers are returned. If false, only one-time purchase products are returned. | [optional]  |
| **isArchived** | **bool?** | Filter by archived status. | [optional]  |
| **query** | **string** | Filter by product name (fuzzy, case-insensitive). | [optional]  |
| **id** | **string** | Filter by product ID. | [optional]  |

### Return type

[**ProductsList200Response**](ProductsList200Response.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved products list. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="productsunarchive"></a>
# **ProductsUnarchive**
> ProductsUnarchive200Response ProductsUnarchive (string id)

Unarchive Product

Restore an archived product back to active status, making it visible again.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class ProductsUnarchiveExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new ProductsApi(config);
            var id = prod_123;  // string | The unique product ID to unarchive.

            try
            {
                // Unarchive Product
                ProductsUnarchive200Response result = apiInstance.ProductsUnarchive(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductsApi.ProductsUnarchive: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ProductsUnarchiveWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Unarchive Product
    ApiResponse<ProductsUnarchive200Response> response = apiInstance.ProductsUnarchiveWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductsApi.ProductsUnarchiveWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The unique product ID to unarchive. |  |

### Return type

[**ProductsUnarchive200Response**](ProductsUnarchive200Response.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Product unarchived successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="productsupdate"></a>
# **ProductsUpdate**
> ProductMessageResponseDto ProductsUpdate (string id, ProductUpdate productUpdate)

Update Product

Update details of an existing product.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class ProductsUpdateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new ProductsApi(config);
            var id = prod_123;  // string | The unique product ID.
            var productUpdate = new ProductUpdate(); // ProductUpdate | 

            try
            {
                // Update Product
                ProductMessageResponseDto result = apiInstance.ProductsUpdate(id, productUpdate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ProductsApi.ProductsUpdate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ProductsUpdateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Product
    ApiResponse<ProductMessageResponseDto> response = apiInstance.ProductsUpdateWithHttpInfo(id, productUpdate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ProductsApi.ProductsUpdateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The unique product ID. |  |
| **productUpdate** | [**ProductUpdate**](ProductUpdate.md) |  |  |

### Return type

[**ProductMessageResponseDto**](ProductMessageResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Product updated successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

