# Solifyn.Api.OrdersApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**OrdersGet**](OrdersApi.md#ordersget) | **GET** /v1/orders/{id} | Retrieve Order |
| [**OrdersGetInvoice**](OrdersApi.md#ordersgetinvoice) | **GET** /v1/orders/{id}/invoice | Get Order Invoice |
| [**OrdersList**](OrdersApi.md#orderslist) | **GET** /v1/orders | List Orders |
| [**OrdersUpdate**](OrdersApi.md#ordersupdate) | **PATCH** /v1/orders/{id} | Update Order Billing Address |
| [**RefundsCreate**](OrdersApi.md#refundscreate) | **POST** /v1/orders/{id}/refund | Create Refund |

<a id="ordersget"></a>
# **OrdersGet**
> Order OrdersGet (string id)

Retrieve Order

Retrieve details of a specific order/payment by ID.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class OrdersGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new OrdersApi(config);
            var id = pay_123;  // string | The unique order/payment ID.

            try
            {
                // Retrieve Order
                Order result = apiInstance.OrdersGet(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling OrdersApi.OrdersGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OrdersGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieve Order
    ApiResponse<Order> response = apiInstance.OrdersGetWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling OrdersApi.OrdersGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The unique order/payment ID. |  |

### Return type

[**Order**](Order.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Order resolved successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="ordersgetinvoice"></a>
# **OrdersGetInvoice**
> Invoice OrdersGetInvoice (string id)

Get Order Invoice

Retrieve the generated invoice details for the specified order.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class OrdersGetInvoiceExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            var apiInstance = new OrdersApi(config);
            var id = pay_123;  // string | The unique order/payment ID.

            try
            {
                // Get Order Invoice
                Invoice result = apiInstance.OrdersGetInvoice(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling OrdersApi.OrdersGetInvoice: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OrdersGetInvoiceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Order Invoice
    ApiResponse<Invoice> response = apiInstance.OrdersGetInvoiceWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling OrdersApi.OrdersGetInvoiceWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The unique order/payment ID. |  |

### Return type

[**Invoice**](Invoice.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Invoice retrieved successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="orderslist"></a>
# **OrdersList**
> OrderList OrdersList (string createdAtLte = null, string createdAtGte = null, string productId = null, string customerId = null, string status = null, decimal? pageSize = null, decimal? pageNumber = null)

List Orders

List and query orders/payments belonging to your active business.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class OrdersListExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new OrdersApi(config);
            var createdAtLte = "createdAtLte_example";  // string | Filter by creation date less than or equal to. (optional) 
            var createdAtGte = "createdAtGte_example";  // string | Filter by creation date greater than or equal to. (optional) 
            var productId = "productId_example";  // string | Filter by product identifier. (optional) 
            var customerId = "customerId_example";  // string | Filter by customer identifier. (optional) 
            var status = "status_example";  // string | Filter by order/payment status. (optional) 
            var pageSize = 10MD;  // decimal? | Size of a page, defaults to 10. Maximum is 100. (optional)  (default to 10M)
            var pageNumber = 1MD;  // decimal? | Page number, defaults to 1. (optional)  (default to 1M)

            try
            {
                // List Orders
                OrderList result = apiInstance.OrdersList(createdAtLte, createdAtGte, productId, customerId, status, pageSize, pageNumber);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling OrdersApi.OrdersList: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OrdersListWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Orders
    ApiResponse<OrderList> response = apiInstance.OrdersListWithHttpInfo(createdAtLte, createdAtGte, productId, customerId, status, pageSize, pageNumber);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling OrdersApi.OrdersListWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createdAtLte** | **string** | Filter by creation date less than or equal to. | [optional]  |
| **createdAtGte** | **string** | Filter by creation date greater than or equal to. | [optional]  |
| **productId** | **string** | Filter by product identifier. | [optional]  |
| **customerId** | **string** | Filter by customer identifier. | [optional]  |
| **status** | **string** | Filter by order/payment status. | [optional]  |
| **pageSize** | **decimal?** | Size of a page, defaults to 10. Maximum is 100. | [optional] [default to 10M] |
| **pageNumber** | **decimal?** | Page number, defaults to 1. | [optional] [default to 1M] |

### Return type

[**OrderList**](OrderList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | List of orders/payments retrieved successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="ordersupdate"></a>
# **OrdersUpdate**
> Order OrdersUpdate (string id, OrderUpdate orderUpdate)

Update Order Billing Address

Update the billing details of an existing order.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class OrdersUpdateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new OrdersApi(config);
            var id = pay_123;  // string | The unique order/payment ID.
            var orderUpdate = new OrderUpdate(); // OrderUpdate | 

            try
            {
                // Update Order Billing Address
                Order result = apiInstance.OrdersUpdate(id, orderUpdate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling OrdersApi.OrdersUpdate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the OrdersUpdateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Order Billing Address
    ApiResponse<Order> response = apiInstance.OrdersUpdateWithHttpInfo(id, orderUpdate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling OrdersApi.OrdersUpdateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The unique order/payment ID. |  |
| **orderUpdate** | [**OrderUpdate**](OrderUpdate.md) |  |  |

### Return type

[**Order**](Order.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Order billing address updated successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="refundscreate"></a>
# **RefundsCreate**
> void RefundsCreate (string id, OrderRefundCreate orderRefundCreate)

Create Refund

Initiate a full or partial refund for a specific payment/order.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class RefundsCreateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new OrdersApi(config);
            var id = pay_123;  // string | The unique order/payment ID.
            var orderRefundCreate = new OrderRefundCreate(); // OrderRefundCreate | 

            try
            {
                // Create Refund
                apiInstance.RefundsCreate(id, orderRefundCreate);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling OrdersApi.RefundsCreate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RefundsCreateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Refund
    apiInstance.RefundsCreateWithHttpInfo(id, orderRefundCreate);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling OrdersApi.RefundsCreateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The unique order/payment ID. |  |
| **orderRefundCreate** | [**OrderRefundCreate**](OrderRefundCreate.md) |  |  |

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Refund processed successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

