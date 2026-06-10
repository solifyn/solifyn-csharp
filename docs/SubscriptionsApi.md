# Solifyn.Api.SubscriptionsApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**SubscriptionsAction**](SubscriptionsApi.md#subscriptionsaction) | **POST** /v1/subscriptions/{subscriptionId}/{action} | Subscription Action |
| [**SubscriptionsGet**](SubscriptionsApi.md#subscriptionsget) | **GET** /v1/subscriptions/{id} | Retrieve Subscription Details |
| [**SubscriptionsList**](SubscriptionsApi.md#subscriptionslist) | **GET** /v1/subscriptions | List Subscriptions |

<a id="subscriptionsaction"></a>
# **SubscriptionsAction**
> SubscriptionsAction201Response SubscriptionsAction (string subscriptionId, string action, SubscriptionAction subscriptionAction)

Subscription Action

Cancel, pause, resume, or add free days to a customer subscription.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class SubscriptionsActionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new SubscriptionsApi(config);
            var subscriptionId = mem_123;  // string | The customer subscription ID
            var action = "add_free_days";  // string | The subscription task to execute
            var subscriptionAction = new SubscriptionAction(); // SubscriptionAction | 

            try
            {
                // Subscription Action
                SubscriptionsAction201Response result = apiInstance.SubscriptionsAction(subscriptionId, action, subscriptionAction);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SubscriptionsApi.SubscriptionsAction: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SubscriptionsActionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Subscription Action
    ApiResponse<SubscriptionsAction201Response> response = apiInstance.SubscriptionsActionWithHttpInfo(subscriptionId, action, subscriptionAction);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SubscriptionsApi.SubscriptionsActionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **subscriptionId** | **string** | The customer subscription ID |  |
| **action** | **string** | The subscription task to execute |  |
| **subscriptionAction** | [**SubscriptionAction**](SubscriptionAction.md) |  |  |

### Return type

[**SubscriptionsAction201Response**](SubscriptionsAction201Response.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Subscription action processed successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="subscriptionsget"></a>
# **SubscriptionsGet**
> SubscriptionDetail SubscriptionsGet (string id)

Retrieve Subscription Details

Retrieve detailed information about a subscription and its billing history.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class SubscriptionsGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new SubscriptionsApi(config);
            var id = mem_123;  // string | The customer subscription ID

            try
            {
                // Retrieve Subscription Details
                SubscriptionDetail result = apiInstance.SubscriptionsGet(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SubscriptionsApi.SubscriptionsGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SubscriptionsGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieve Subscription Details
    ApiResponse<SubscriptionDetail> response = apiInstance.SubscriptionsGetWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SubscriptionsApi.SubscriptionsGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The customer subscription ID |  |

### Return type

[**SubscriptionDetail**](SubscriptionDetail.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Subscription details retrieved successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="subscriptionslist"></a>
# **SubscriptionsList**
> SubscriptionList SubscriptionsList (string customerId = null)

List Subscriptions

Retrieve a list of customer subscriptions, optionally filtered by customer ID.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class SubscriptionsListExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new SubscriptionsApi(config);
            var customerId = "customerId_example";  // string | Filter subscriptions by customer ID. (optional) 

            try
            {
                // List Subscriptions
                SubscriptionList result = apiInstance.SubscriptionsList(customerId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SubscriptionsApi.SubscriptionsList: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SubscriptionsListWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Subscriptions
    ApiResponse<SubscriptionList> response = apiInstance.SubscriptionsListWithHttpInfo(customerId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SubscriptionsApi.SubscriptionsListWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **customerId** | **string** | Filter subscriptions by customer ID. | [optional]  |

### Return type

[**SubscriptionList**](SubscriptionList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Subscriptions retrieved successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

