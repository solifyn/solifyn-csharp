# Solifyn.Api.DiscountsApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**DiscountsCreate**](DiscountsApi.md#discountscreate) | **POST** /v1/discounts | Create Discount |
| [**DiscountsDelete**](DiscountsApi.md#discountsdelete) | **DELETE** /v1/discounts/{id} | Delete Discount |
| [**DiscountsGet**](DiscountsApi.md#discountsget) | **GET** /v1/discounts/{id} | Retrieve Discount |
| [**DiscountsList**](DiscountsApi.md#discountslist) | **GET** /v1/discounts | List Discounts |
| [**DiscountsUpdate**](DiscountsApi.md#discountsupdate) | **PATCH** /v1/discounts/{id} | Update Discount |
| [**DiscountsValidate**](DiscountsApi.md#discountsvalidate) | **GET** /v1/discounts/validate | Validate Code |

<a id="discountscreate"></a>
# **DiscountsCreate**
> Discount DiscountsCreate (DiscountCreate discountCreate)

Create Discount

Create a new discount code within your active business.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class DiscountsCreateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DiscountsApi(config);
            var discountCreate = new DiscountCreate(); // DiscountCreate | 

            try
            {
                // Create Discount
                Discount result = apiInstance.DiscountsCreate(discountCreate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DiscountsApi.DiscountsCreate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DiscountsCreateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Discount
    ApiResponse<Discount> response = apiInstance.DiscountsCreateWithHttpInfo(discountCreate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DiscountsApi.DiscountsCreateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **discountCreate** | [**DiscountCreate**](DiscountCreate.md) |  |  |

### Return type

[**Discount**](Discount.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Discount created successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="discountsdelete"></a>
# **DiscountsDelete**
> LicensesDeactivate200Response DiscountsDelete (string id)

Delete Discount

Delete a specific discount code by ID.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class DiscountsDeleteExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DiscountsApi(config);
            var id = disc_123;  // string | The unique discount ID.

            try
            {
                // Delete Discount
                LicensesDeactivate200Response result = apiInstance.DiscountsDelete(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DiscountsApi.DiscountsDelete: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DiscountsDeleteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete Discount
    ApiResponse<LicensesDeactivate200Response> response = apiInstance.DiscountsDeleteWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DiscountsApi.DiscountsDeleteWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The unique discount ID. |  |

### Return type

[**LicensesDeactivate200Response**](LicensesDeactivate200Response.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Discount deleted successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="discountsget"></a>
# **DiscountsGet**
> Discount DiscountsGet (string id)

Retrieve Discount

Retrieve details of a specific discount code using its ID.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class DiscountsGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DiscountsApi(config);
            var id = disc_123;  // string | The unique discount ID.

            try
            {
                // Retrieve Discount
                Discount result = apiInstance.DiscountsGet(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DiscountsApi.DiscountsGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DiscountsGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieve Discount
    ApiResponse<Discount> response = apiInstance.DiscountsGetWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DiscountsApi.DiscountsGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The unique discount ID. |  |

### Return type

[**Discount**](Discount.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved discount details. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="discountslist"></a>
# **DiscountsList**
> DiscountsList200Response DiscountsList (string sorting = null, decimal? limit = null, decimal? page = null, string query = null, string id = null)

List Discounts

List and query discounts belonging to your active business with support for fuzzy search by code, pagination, and sorting.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class DiscountsListExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DiscountsApi(config);
            var sorting = "created_at";  // string | Sorting criterion. Add a minus sign - before the criteria name to sort by descending order. (optional) 
            var limit = 10MD;  // decimal? | Size of a page, defaults to 10. Maximum is 100. (optional)  (default to 10M)
            var page = 1MD;  // decimal? | Page number, defaults to 1. (optional)  (default to 1M)
            var query = "query_example";  // string | Filter by discount code (fuzzy, case-insensitive). (optional) 
            var id = "id_example";  // string | Filter by discount ID. (optional) 

            try
            {
                // List Discounts
                DiscountsList200Response result = apiInstance.DiscountsList(sorting, limit, page, query, id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DiscountsApi.DiscountsList: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DiscountsListWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Discounts
    ApiResponse<DiscountsList200Response> response = apiInstance.DiscountsListWithHttpInfo(sorting, limit, page, query, id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DiscountsApi.DiscountsListWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **sorting** | **string** | Sorting criterion. Add a minus sign - before the criteria name to sort by descending order. | [optional]  |
| **limit** | **decimal?** | Size of a page, defaults to 10. Maximum is 100. | [optional] [default to 10M] |
| **page** | **decimal?** | Page number, defaults to 1. | [optional] [default to 1M] |
| **query** | **string** | Filter by discount code (fuzzy, case-insensitive). | [optional]  |
| **id** | **string** | Filter by discount ID. | [optional]  |

### Return type

[**DiscountsList200Response**](DiscountsList200Response.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successfully retrieved discounts list. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="discountsupdate"></a>
# **DiscountsUpdate**
> Discount DiscountsUpdate (string id, DiscountUpdate discountUpdate)

Update Discount

Update details of an existing discount code.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class DiscountsUpdateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DiscountsApi(config);
            var id = disc_123;  // string | The unique discount ID.
            var discountUpdate = new DiscountUpdate(); // DiscountUpdate | 

            try
            {
                // Update Discount
                Discount result = apiInstance.DiscountsUpdate(id, discountUpdate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DiscountsApi.DiscountsUpdate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DiscountsUpdateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Discount
    ApiResponse<Discount> response = apiInstance.DiscountsUpdateWithHttpInfo(id, discountUpdate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DiscountsApi.DiscountsUpdateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The unique discount ID. |  |
| **discountUpdate** | [**DiscountUpdate**](DiscountUpdate.md) |  |  |

### Return type

[**Discount**](Discount.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Discount updated successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="discountsvalidate"></a>
# **DiscountsValidate**
> Discount DiscountsValidate (string code, string businessId)

Validate Code

Validate if a specific discount code is active and valid for purchase checkout.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class DiscountsValidateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DiscountsApi(config);
            var code = SAVE20;  // string | The plain discount code string
            var businessId = biz_123;  // string | The business database ID context

            try
            {
                // Validate Code
                Discount result = apiInstance.DiscountsValidate(code, businessId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DiscountsApi.DiscountsValidate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DiscountsValidateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Validate Code
    ApiResponse<Discount> response = apiInstance.DiscountsValidateWithHttpInfo(code, businessId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DiscountsApi.DiscountsValidateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **code** | **string** | The plain discount code string |  |
| **businessId** | **string** | The business database ID context |  |

### Return type

[**Discount**](Discount.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Validation query results. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

