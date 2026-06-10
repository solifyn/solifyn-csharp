# Solifyn.Api.WebhookApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**WebhookControllerHandleSvixWebhook**](WebhookApi.md#webhookcontrollerhandlesvixwebhook) | **POST** /v1/webhook/svix |  |
| [**WebhookControllerHandleWebhook**](WebhookApi.md#webhookcontrollerhandlewebhook) | **POST** /v1/webhook |  |

<a id="webhookcontrollerhandlesvixwebhook"></a>
# **WebhookControllerHandleSvixWebhook**
> void WebhookControllerHandleSvixWebhook ()



### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class WebhookControllerHandleSvixWebhookExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            var apiInstance = new WebhookApi(config);

            try
            {
                apiInstance.WebhookControllerHandleSvixWebhook();
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookApi.WebhookControllerHandleSvixWebhook: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WebhookControllerHandleSvixWebhookWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.WebhookControllerHandleSvixWebhookWithHttpInfo();
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookApi.WebhookControllerHandleSvixWebhookWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="webhookcontrollerhandlewebhook"></a>
# **WebhookControllerHandleWebhook**
> void WebhookControllerHandleWebhook (string businessId)



### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class WebhookControllerHandleWebhookExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            var apiInstance = new WebhookApi(config);
            var businessId = "businessId_example";  // string | 

            try
            {
                apiInstance.WebhookControllerHandleWebhook(businessId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhookApi.WebhookControllerHandleWebhook: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WebhookControllerHandleWebhookWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.WebhookControllerHandleWebhookWithHttpInfo(businessId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhookApi.WebhookControllerHandleWebhookWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **businessId** | **string** |  |  |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

