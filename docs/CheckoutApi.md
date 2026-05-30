# Solifyn.Api.CheckoutApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CheckoutCreate**](CheckoutApi.md#checkoutcreate) | **POST** /v1/checkout/create | Create Checkout Session |
| [**CheckoutCreateCollection**](CheckoutApi.md#checkoutcreatecollection) | **POST** /v1/checkout/collection/create | Create Collection Checkout Session |
| [**CheckoutGetSession**](CheckoutApi.md#checkoutgetsession) | **GET** /v1/checkout/session/{id} | Get Checkout Session Details |
| [**CheckoutPricePreview**](CheckoutApi.md#checkoutpricepreview) | **GET** /v1/checkout/price-preview | Get Converted Price Preview |
| [**CheckoutSupportedCurrencies**](CheckoutApi.md#checkoutsupportedcurrencies) | **GET** /v1/checkout/supported-currencies | Get Supported Currencies |

<a id="checkoutcreate"></a>
# **CheckoutCreate**
> CheckoutResponseDto CheckoutCreate (CreateCheckoutDto createCheckoutDto)

Create Checkout Session

Create a new payment configuration for a product. Returns redirect URLs pointing to the custom checkout layout.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class CheckoutCreateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            var apiInstance = new CheckoutApi(config);
            var createCheckoutDto = new CreateCheckoutDto(); // CreateCheckoutDto | 

            try
            {
                // Create Checkout Session
                CheckoutResponseDto result = apiInstance.CheckoutCreate(createCheckoutDto);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CheckoutApi.CheckoutCreate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CheckoutCreateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Checkout Session
    ApiResponse<CheckoutResponseDto> response = apiInstance.CheckoutCreateWithHttpInfo(createCheckoutDto);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CheckoutApi.CheckoutCreateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createCheckoutDto** | [**CreateCheckoutDto**](CreateCheckoutDto.md) |  |  |

### Return type

[**CheckoutResponseDto**](CheckoutResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Checkout session configuration created successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="checkoutcreatecollection"></a>
# **CheckoutCreateCollection**
> CheckoutResponseDto CheckoutCreateCollection (CreateCollectionCheckoutDto createCollectionCheckoutDto)

Create Collection Checkout Session

Create a new payment configuration for a product bundle/collection.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class CheckoutCreateCollectionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            var apiInstance = new CheckoutApi(config);
            var createCollectionCheckoutDto = new CreateCollectionCheckoutDto(); // CreateCollectionCheckoutDto | 

            try
            {
                // Create Collection Checkout Session
                CheckoutResponseDto result = apiInstance.CheckoutCreateCollection(createCollectionCheckoutDto);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CheckoutApi.CheckoutCreateCollection: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CheckoutCreateCollectionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Collection Checkout Session
    ApiResponse<CheckoutResponseDto> response = apiInstance.CheckoutCreateCollectionWithHttpInfo(createCollectionCheckoutDto);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CheckoutApi.CheckoutCreateCollectionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createCollectionCheckoutDto** | [**CreateCollectionCheckoutDto**](CreateCollectionCheckoutDto.md) |  |  |

### Return type

[**CheckoutResponseDto**](CheckoutResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Collection checkout session created. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="checkoutgetsession"></a>
# **CheckoutGetSession**
> CheckoutSessionDetailsDto CheckoutGetSession (string id)

Get Checkout Session Details

Retrieve checkout details to mount the custom embedded checkout.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class CheckoutGetSessionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            var apiInstance = new CheckoutApi(config);
            var id = ch_XXXXXXXXXXX;  // string | Internal database checkout session ID

            try
            {
                // Get Checkout Session Details
                CheckoutSessionDetailsDto result = apiInstance.CheckoutGetSession(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CheckoutApi.CheckoutGetSession: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CheckoutGetSessionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Checkout Session Details
    ApiResponse<CheckoutSessionDetailsDto> response = apiInstance.CheckoutGetSessionWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CheckoutApi.CheckoutGetSessionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | Internal database checkout session ID |  |

### Return type

[**CheckoutSessionDetailsDto**](CheckoutSessionDetailsDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Checkout session details resolved. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="checkoutpricepreview"></a>
# **CheckoutPricePreview**
> PricePreviewResponseDto CheckoutPricePreview (string productId, string addons, string currency = null, string discount = null, string qty = null, string customPrice = null)

Get Converted Price Preview

Pre-calculate target currencies, applied discounts, and PWYW values before mounting the checkout.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class CheckoutPricePreviewExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            var apiInstance = new CheckoutApi(config);
            var productId = prod_z2o92kEl6cYYX;  // string | Public product ID
            var addons = "addons_example";  // string | 
            var currency = vnd;  // string | Target currency code (ISO) (optional) 
            var discount = 10;  // string | Percentage discount rate (optional) 
            var qty = 1;  // string | Number of product units (optional) 
            var customPrice = 15;  // string | Override price for PWYW products (optional) 

            try
            {
                // Get Converted Price Preview
                PricePreviewResponseDto result = apiInstance.CheckoutPricePreview(productId, addons, currency, discount, qty, customPrice);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CheckoutApi.CheckoutPricePreview: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CheckoutPricePreviewWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Converted Price Preview
    ApiResponse<PricePreviewResponseDto> response = apiInstance.CheckoutPricePreviewWithHttpInfo(productId, addons, currency, discount, qty, customPrice);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CheckoutApi.CheckoutPricePreviewWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **productId** | **string** | Public product ID |  |
| **addons** | **string** |  |  |
| **currency** | **string** | Target currency code (ISO) | [optional]  |
| **discount** | **string** | Percentage discount rate | [optional]  |
| **qty** | **string** | Number of product units | [optional]  |
| **customPrice** | **string** | Override price for PWYW products | [optional]  |

### Return type

[**PricePreviewResponseDto**](PricePreviewResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Price preview calculations returned. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="checkoutsupportedcurrencies"></a>
# **CheckoutSupportedCurrencies**
> List&lt;SupportedCurrenciesResponseDto&gt; CheckoutSupportedCurrencies ()

Get Supported Currencies

Retrieve all currencies supported for payouts and conversions.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class CheckoutSupportedCurrenciesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            var apiInstance = new CheckoutApi(config);

            try
            {
                // Get Supported Currencies
                List<SupportedCurrenciesResponseDto> result = apiInstance.CheckoutSupportedCurrencies();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CheckoutApi.CheckoutSupportedCurrencies: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CheckoutSupportedCurrenciesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Supported Currencies
    ApiResponse<List<SupportedCurrenciesResponseDto>> response = apiInstance.CheckoutSupportedCurrenciesWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CheckoutApi.CheckoutSupportedCurrenciesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**List&lt;SupportedCurrenciesResponseDto&gt;**](SupportedCurrenciesResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Supported currencies resolved successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

