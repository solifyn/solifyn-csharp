# Solifyn.Api.CollectionsApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CollectionsAddProducts**](CollectionsApi.md#collectionsaddproducts) | **POST** /v1/collections/{id}/products | Add Products to Collection |
| [**CollectionsArchive**](CollectionsApi.md#collectionsarchive) | **DELETE** /v1/collections/{id} | Archive Collection |
| [**CollectionsCreate**](CollectionsApi.md#collectionscreate) | **POST** /v1/collections | Create Collection |
| [**CollectionsDeleteProduct**](CollectionsApi.md#collectionsdeleteproduct) | **DELETE** /v1/collections/{id}/products/{productId} | Remove Product from Collection |
| [**CollectionsGet**](CollectionsApi.md#collectionsget) | **GET** /v1/collections/{id} | Retrieve Collection |
| [**CollectionsList**](CollectionsApi.md#collectionslist) | **GET** /v1/collections | List Collections |
| [**CollectionsListArchived**](CollectionsApi.md#collectionslistarchived) | **GET** /v1/collections/archived | List Archived Collections |
| [**CollectionsUnarchive**](CollectionsApi.md#collectionsunarchive) | **POST** /v1/collections/{id}/unarchive | Unarchive Collection |
| [**CollectionsUpdate**](CollectionsApi.md#collectionsupdate) | **PATCH** /v1/collections/{id} | Update Collection |
| [**CollectionsUpdateProduct**](CollectionsApi.md#collectionsupdateproduct) | **PATCH** /v1/collections/{id}/products/{productId} | Update Collection Product |

<a id="collectionsaddproducts"></a>
# **CollectionsAddProducts**
> CollectionResponseDto CollectionsAddProducts (string id, AddCollectionProductsDto addCollectionProductsDto)

Add Products to Collection

Add one or more products to a collection. If a product already exists, its quantity is updated.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class CollectionsAddProductsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new CollectionsApi(config);
            var id = col_123;  // string | Collection ID
            var addCollectionProductsDto = new AddCollectionProductsDto(); // AddCollectionProductsDto | 

            try
            {
                // Add Products to Collection
                CollectionResponseDto result = apiInstance.CollectionsAddProducts(id, addCollectionProductsDto);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CollectionsApi.CollectionsAddProducts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CollectionsAddProductsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Add Products to Collection
    ApiResponse<CollectionResponseDto> response = apiInstance.CollectionsAddProductsWithHttpInfo(id, addCollectionProductsDto);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CollectionsApi.CollectionsAddProductsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | Collection ID |  |
| **addCollectionProductsDto** | [**AddCollectionProductsDto**](AddCollectionProductsDto.md) |  |  |

### Return type

[**CollectionResponseDto**](CollectionResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Products added/updated successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="collectionsarchive"></a>
# **CollectionsArchive**
> CollectionArchivedResponseDto CollectionsArchive (string id)

Archive Collection

Deactivate and move a collection to archives.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class CollectionsArchiveExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new CollectionsApi(config);
            var id = col_123;  // string | Collection ID

            try
            {
                // Archive Collection
                CollectionArchivedResponseDto result = apiInstance.CollectionsArchive(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CollectionsApi.CollectionsArchive: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CollectionsArchiveWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Archive Collection
    ApiResponse<CollectionArchivedResponseDto> response = apiInstance.CollectionsArchiveWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CollectionsApi.CollectionsArchiveWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | Collection ID |  |

### Return type

[**CollectionArchivedResponseDto**](CollectionArchivedResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Collection archived successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="collectionscreate"></a>
# **CollectionsCreate**
> CollectionResponseDto CollectionsCreate (CreateCollectionDto createCollectionDto)

Create Collection

Generate a new product collection for checkout packaging.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class CollectionsCreateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new CollectionsApi(config);
            var createCollectionDto = new CreateCollectionDto(); // CreateCollectionDto | 

            try
            {
                // Create Collection
                CollectionResponseDto result = apiInstance.CollectionsCreate(createCollectionDto);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CollectionsApi.CollectionsCreate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CollectionsCreateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Collection
    ApiResponse<CollectionResponseDto> response = apiInstance.CollectionsCreateWithHttpInfo(createCollectionDto);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CollectionsApi.CollectionsCreateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createCollectionDto** | [**CreateCollectionDto**](CreateCollectionDto.md) |  |  |

### Return type

[**CollectionResponseDto**](CollectionResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Collection created successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="collectionsdeleteproduct"></a>
# **CollectionsDeleteProduct**
> CollectionProductDeletedResponseDto CollectionsDeleteProduct (string id, string productId)

Remove Product from Collection

Remove a product from a collection.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class CollectionsDeleteProductExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new CollectionsApi(config);
            var id = col_123;  // string | Collection ID
            var productId = prod_123;  // string | Product ID

            try
            {
                // Remove Product from Collection
                CollectionProductDeletedResponseDto result = apiInstance.CollectionsDeleteProduct(id, productId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CollectionsApi.CollectionsDeleteProduct: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CollectionsDeleteProductWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Remove Product from Collection
    ApiResponse<CollectionProductDeletedResponseDto> response = apiInstance.CollectionsDeleteProductWithHttpInfo(id, productId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CollectionsApi.CollectionsDeleteProductWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | Collection ID |  |
| **productId** | **string** | Product ID |  |

### Return type

[**CollectionProductDeletedResponseDto**](CollectionProductDeletedResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Product removed from collection successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="collectionsget"></a>
# **CollectionsGet**
> CollectionDetailResponseDto CollectionsGet (string id)

Retrieve Collection

Get properties of a product collection by ID.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class CollectionsGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new CollectionsApi(config);
            var id = col_123;  // string | Collection ID

            try
            {
                // Retrieve Collection
                CollectionDetailResponseDto result = apiInstance.CollectionsGet(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CollectionsApi.CollectionsGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CollectionsGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieve Collection
    ApiResponse<CollectionDetailResponseDto> response = apiInstance.CollectionsGetWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CollectionsApi.CollectionsGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | Collection ID |  |

### Return type

[**CollectionDetailResponseDto**](CollectionDetailResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Collection details retrieved successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="collectionslist"></a>
# **CollectionsList**
> List&lt;CollectionResponseDto&gt; CollectionsList ()

List Collections

Get all active product collections linked to the current active business.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class CollectionsListExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new CollectionsApi(config);

            try
            {
                // List Collections
                List<CollectionResponseDto> result = apiInstance.CollectionsList();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CollectionsApi.CollectionsList: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CollectionsListWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Collections
    ApiResponse<List<CollectionResponseDto>> response = apiInstance.CollectionsListWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CollectionsApi.CollectionsListWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**List&lt;CollectionResponseDto&gt;**](CollectionResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Collections retrieved successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="collectionslistarchived"></a>
# **CollectionsListArchived**
> List&lt;CollectionResponseDto&gt; CollectionsListArchived ()

List Archived Collections

Get all archived/deactivated product collections.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class CollectionsListArchivedExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new CollectionsApi(config);

            try
            {
                // List Archived Collections
                List<CollectionResponseDto> result = apiInstance.CollectionsListArchived();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CollectionsApi.CollectionsListArchived: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CollectionsListArchivedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Archived Collections
    ApiResponse<List<CollectionResponseDto>> response = apiInstance.CollectionsListArchivedWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CollectionsApi.CollectionsListArchivedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**List&lt;CollectionResponseDto&gt;**](CollectionResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Archived collections list retrieved. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="collectionsunarchive"></a>
# **CollectionsUnarchive**
> CollectionUnarchivedResponseDto CollectionsUnarchive (string id)

Unarchive Collection

Restore an archived collection back to active status.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class CollectionsUnarchiveExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new CollectionsApi(config);
            var id = col_123;  // string | Collection ID

            try
            {
                // Unarchive Collection
                CollectionUnarchivedResponseDto result = apiInstance.CollectionsUnarchive(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CollectionsApi.CollectionsUnarchive: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CollectionsUnarchiveWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Unarchive Collection
    ApiResponse<CollectionUnarchivedResponseDto> response = apiInstance.CollectionsUnarchiveWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CollectionsApi.CollectionsUnarchiveWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | Collection ID |  |

### Return type

[**CollectionUnarchivedResponseDto**](CollectionUnarchivedResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Collection unarchived successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="collectionsupdate"></a>
# **CollectionsUpdate**
> CollectionUpdatedResponseDto CollectionsUpdate (string id, UpdateCollectionDto updateCollectionDto)

Update Collection

Update products, friendly name, status, or description of a collection.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class CollectionsUpdateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new CollectionsApi(config);
            var id = col_123;  // string | Collection ID
            var updateCollectionDto = new UpdateCollectionDto(); // UpdateCollectionDto | 

            try
            {
                // Update Collection
                CollectionUpdatedResponseDto result = apiInstance.CollectionsUpdate(id, updateCollectionDto);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CollectionsApi.CollectionsUpdate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CollectionsUpdateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Collection
    ApiResponse<CollectionUpdatedResponseDto> response = apiInstance.CollectionsUpdateWithHttpInfo(id, updateCollectionDto);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CollectionsApi.CollectionsUpdateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | Collection ID |  |
| **updateCollectionDto** | [**UpdateCollectionDto**](UpdateCollectionDto.md) |  |  |

### Return type

[**CollectionUpdatedResponseDto**](CollectionUpdatedResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Collection updated successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="collectionsupdateproduct"></a>
# **CollectionsUpdateProduct**
> CollectionProductUpdatedResponseDto CollectionsUpdateProduct (string id, string productId, UpdateCollectionProductDto updateCollectionProductDto)

Update Collection Product

Update quantity of a specific product inside a collection.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class CollectionsUpdateProductExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new CollectionsApi(config);
            var id = col_123;  // string | Collection ID
            var productId = prod_123;  // string | Product ID
            var updateCollectionProductDto = new UpdateCollectionProductDto(); // UpdateCollectionProductDto | 

            try
            {
                // Update Collection Product
                CollectionProductUpdatedResponseDto result = apiInstance.CollectionsUpdateProduct(id, productId, updateCollectionProductDto);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CollectionsApi.CollectionsUpdateProduct: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CollectionsUpdateProductWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Collection Product
    ApiResponse<CollectionProductUpdatedResponseDto> response = apiInstance.CollectionsUpdateProductWithHttpInfo(id, productId, updateCollectionProductDto);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CollectionsApi.CollectionsUpdateProductWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | Collection ID |  |
| **productId** | **string** | Product ID |  |
| **updateCollectionProductDto** | [**UpdateCollectionProductDto**](UpdateCollectionProductDto.md) |  |  |

### Return type

[**CollectionProductUpdatedResponseDto**](CollectionProductUpdatedResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Collection product quantity updated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

