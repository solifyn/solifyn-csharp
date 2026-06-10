# Solifyn.Api.CheckoutLinksApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CheckoutLinksCreate**](CheckoutLinksApi.md#checkoutlinkscreate) | **POST** /v1/checkout-links | Create Checkout Link |
| [**CheckoutLinksDelete**](CheckoutLinksApi.md#checkoutlinksdelete) | **DELETE** /v1/checkout-links/{id} | Delete Checkout Link |
| [**CheckoutLinksGet**](CheckoutLinksApi.md#checkoutlinksget) | **GET** /v1/checkout-links/{id} | Retrieve Checkout Link Details |
| [**CheckoutLinksList**](CheckoutLinksApi.md#checkoutlinkslist) | **GET** /v1/checkout-links | List Checkout Links |
| [**CheckoutLinksUpdate**](CheckoutLinksApi.md#checkoutlinksupdate) | **PATCH** /v1/checkout-links/{id} | Update Checkout Link |

<a id="checkoutlinkscreate"></a>
# **CheckoutLinksCreate**
> CheckoutLinkResponseDto CheckoutLinksCreate (CreateCheckoutLinkDto createCheckoutLinkDto)

Create Checkout Link

Generate a new checkout session link.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class CheckoutLinksCreateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new CheckoutLinksApi(config);
            var createCheckoutLinkDto = new CreateCheckoutLinkDto(); // CreateCheckoutLinkDto | 

            try
            {
                // Create Checkout Link
                CheckoutLinkResponseDto result = apiInstance.CheckoutLinksCreate(createCheckoutLinkDto);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CheckoutLinksApi.CheckoutLinksCreate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CheckoutLinksCreateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Checkout Link
    ApiResponse<CheckoutLinkResponseDto> response = apiInstance.CheckoutLinksCreateWithHttpInfo(createCheckoutLinkDto);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CheckoutLinksApi.CheckoutLinksCreateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createCheckoutLinkDto** | [**CreateCheckoutLinkDto**](CreateCheckoutLinkDto.md) |  |  |

### Return type

[**CheckoutLinkResponseDto**](CheckoutLinkResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Checkout link created successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="checkoutlinksdelete"></a>
# **CheckoutLinksDelete**
> CheckoutLinkMessageResponseDto CheckoutLinksDelete (string id)

Delete Checkout Link

Permanently remove a checkout link.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class CheckoutLinksDeleteExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new CheckoutLinksApi(config);
            var id = chk_123;  // string | Checkout Link ID

            try
            {
                // Delete Checkout Link
                CheckoutLinkMessageResponseDto result = apiInstance.CheckoutLinksDelete(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CheckoutLinksApi.CheckoutLinksDelete: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CheckoutLinksDeleteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete Checkout Link
    ApiResponse<CheckoutLinkMessageResponseDto> response = apiInstance.CheckoutLinksDeleteWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CheckoutLinksApi.CheckoutLinksDeleteWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | Checkout Link ID |  |

### Return type

[**CheckoutLinkMessageResponseDto**](CheckoutLinkMessageResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Checkout link deleted successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="checkoutlinksget"></a>
# **CheckoutLinksGet**
> CheckoutLinkResponseDto CheckoutLinksGet (string id)

Retrieve Checkout Link Details

Get details of a specific checkout link by ID (public access).

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class CheckoutLinksGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new CheckoutLinksApi(config);
            var id = chk_123;  // string | Checkout Link ID

            try
            {
                // Retrieve Checkout Link Details
                CheckoutLinkResponseDto result = apiInstance.CheckoutLinksGet(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CheckoutLinksApi.CheckoutLinksGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CheckoutLinksGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieve Checkout Link Details
    ApiResponse<CheckoutLinkResponseDto> response = apiInstance.CheckoutLinksGetWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CheckoutLinksApi.CheckoutLinksGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | Checkout Link ID |  |

### Return type

[**CheckoutLinkResponseDto**](CheckoutLinkResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Checkout link resolved successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="checkoutlinkslist"></a>
# **CheckoutLinksList**
> List&lt;CheckoutLinkResponseDto&gt; CheckoutLinksList ()

List Checkout Links

Retrieve all active checkout session links for the active business.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class CheckoutLinksListExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new CheckoutLinksApi(config);

            try
            {
                // List Checkout Links
                List<CheckoutLinkResponseDto> result = apiInstance.CheckoutLinksList();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CheckoutLinksApi.CheckoutLinksList: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CheckoutLinksListWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Checkout Links
    ApiResponse<List<CheckoutLinkResponseDto>> response = apiInstance.CheckoutLinksListWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CheckoutLinksApi.CheckoutLinksListWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**List&lt;CheckoutLinkResponseDto&gt;**](CheckoutLinkResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Checkout links retrieved successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="checkoutlinksupdate"></a>
# **CheckoutLinksUpdate**
> CheckoutLinkMessageResponseDto CheckoutLinksUpdate (string id, UpdateCheckoutLinkDto updateCheckoutLinkDto)

Update Checkout Link

Update title, custom pricing, redirection URLs, or friendly inputs for a checkout link.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class CheckoutLinksUpdateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new CheckoutLinksApi(config);
            var id = chk_123;  // string | Checkout Link ID
            var updateCheckoutLinkDto = new UpdateCheckoutLinkDto(); // UpdateCheckoutLinkDto | 

            try
            {
                // Update Checkout Link
                CheckoutLinkMessageResponseDto result = apiInstance.CheckoutLinksUpdate(id, updateCheckoutLinkDto);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CheckoutLinksApi.CheckoutLinksUpdate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CheckoutLinksUpdateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Checkout Link
    ApiResponse<CheckoutLinkMessageResponseDto> response = apiInstance.CheckoutLinksUpdateWithHttpInfo(id, updateCheckoutLinkDto);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CheckoutLinksApi.CheckoutLinksUpdateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | Checkout Link ID |  |
| **updateCheckoutLinkDto** | [**UpdateCheckoutLinkDto**](UpdateCheckoutLinkDto.md) |  |  |

### Return type

[**CheckoutLinkMessageResponseDto**](CheckoutLinkMessageResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Checkout link updated successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

