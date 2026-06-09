# Solifyn.Api.DefaultApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**DisputeCreatedPost**](DefaultApi.md#disputecreatedpost) | **POST** /dispute.created | Dispute Created |
| [**DisputeLostPost**](DefaultApi.md#disputelostpost) | **POST** /dispute.lost | Dispute Lost |
| [**DisputeWonPost**](DefaultApi.md#disputewonpost) | **POST** /dispute.won | Dispute Won |
| [**LicenseCreatedPost**](DefaultApi.md#licensecreatedpost) | **POST** /license.created | License Created |
| [**LicenseRevokedPost**](DefaultApi.md#licenserevokedpost) | **POST** /license.revoked | License Revoked |
| [**PaymentCreatedPost**](DefaultApi.md#paymentcreatedpost) | **POST** /payment.created | Payment Created |
| [**PaymentFailedPost**](DefaultApi.md#paymentfailedpost) | **POST** /payment.failed | Payment Failed |
| [**PaymentSucceededPost**](DefaultApi.md#paymentsucceededpost) | **POST** /payment.succeeded | Payment Succeeded |
| [**RefundFailedPost**](DefaultApi.md#refundfailedpost) | **POST** /refund.failed | Refund Failed |
| [**RefundSucceededPost**](DefaultApi.md#refundsucceededpost) | **POST** /refund.succeeded | Refund Succeeded |
| [**SubscriptionCreatedPost**](DefaultApi.md#subscriptioncreatedpost) | **POST** /subscription.created | Subscription Created |
| [**SubscriptionDeactivatedPost**](DefaultApi.md#subscriptiondeactivatedpost) | **POST** /subscription.deactivated | Subscription Deactivated |
| [**SubscriptionUpdatedPost**](DefaultApi.md#subscriptionupdatedpost) | **POST** /subscription.updated | Subscription Updated |

<a id="disputecreatedpost"></a>
# **DisputeCreatedPost**
> void DisputeCreatedPost (WebhookDisputePayload webhookDisputePayload = null)

Dispute Created

Occurs when a payment charge is disputed by the customer (chargeback initiated).

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class DisputeCreatedPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DefaultApi(config);
            var webhookDisputePayload = new WebhookDisputePayload(); // WebhookDisputePayload |  (optional) 

            try
            {
                // Dispute Created
                apiInstance.DisputeCreatedPost(webhookDisputePayload);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.DisputeCreatedPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DisputeCreatedPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Dispute Created
    apiInstance.DisputeCreatedPostWithHttpInfo(webhookDisputePayload);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.DisputeCreatedPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookDisputePayload** | [**WebhookDisputePayload**](WebhookDisputePayload.md) |  | [optional]  |

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
| **200** | Webhook processed successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="disputelostpost"></a>
# **DisputeLostPost**
> void DisputeLostPost (WebhookDisputePayload webhookDisputePayload = null)

Dispute Lost

Occurs when a dispute challenge is lost and the funds are returned to the cardholder.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class DisputeLostPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DefaultApi(config);
            var webhookDisputePayload = new WebhookDisputePayload(); // WebhookDisputePayload |  (optional) 

            try
            {
                // Dispute Lost
                apiInstance.DisputeLostPost(webhookDisputePayload);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.DisputeLostPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DisputeLostPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Dispute Lost
    apiInstance.DisputeLostPostWithHttpInfo(webhookDisputePayload);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.DisputeLostPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookDisputePayload** | [**WebhookDisputePayload**](WebhookDisputePayload.md) |  | [optional]  |

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
| **200** | Webhook processed successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="disputewonpost"></a>
# **DisputeWonPost**
> void DisputeWonPost (WebhookDisputePayload webhookDisputePayload = null)

Dispute Won

Occurs when a dispute challenge is won by the merchant.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class DisputeWonPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DefaultApi(config);
            var webhookDisputePayload = new WebhookDisputePayload(); // WebhookDisputePayload |  (optional) 

            try
            {
                // Dispute Won
                apiInstance.DisputeWonPost(webhookDisputePayload);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.DisputeWonPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DisputeWonPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Dispute Won
    apiInstance.DisputeWonPostWithHttpInfo(webhookDisputePayload);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.DisputeWonPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookDisputePayload** | [**WebhookDisputePayload**](WebhookDisputePayload.md) |  | [optional]  |

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
| **200** | Webhook processed successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="licensecreatedpost"></a>
# **LicenseCreatedPost**
> void LicenseCreatedPost (WebhookLicensePayload webhookLicensePayload = null)

License Created

Occurs when a new software license key is created or assigned to a customer purchase.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class LicenseCreatedPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DefaultApi(config);
            var webhookLicensePayload = new WebhookLicensePayload(); // WebhookLicensePayload |  (optional) 

            try
            {
                // License Created
                apiInstance.LicenseCreatedPost(webhookLicensePayload);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.LicenseCreatedPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LicenseCreatedPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // License Created
    apiInstance.LicenseCreatedPostWithHttpInfo(webhookLicensePayload);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.LicenseCreatedPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookLicensePayload** | [**WebhookLicensePayload**](WebhookLicensePayload.md) |  | [optional]  |

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
| **200** | Webhook processed successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="licenserevokedpost"></a>
# **LicenseRevokedPost**
> void LicenseRevokedPost (WebhookLicensePayload webhookLicensePayload = null)

License Revoked

Occurs when a software license key is revoked (e.g., due to subscription cancellation, refund, or dispute).

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class LicenseRevokedPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DefaultApi(config);
            var webhookLicensePayload = new WebhookLicensePayload(); // WebhookLicensePayload |  (optional) 

            try
            {
                // License Revoked
                apiInstance.LicenseRevokedPost(webhookLicensePayload);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.LicenseRevokedPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LicenseRevokedPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // License Revoked
    apiInstance.LicenseRevokedPostWithHttpInfo(webhookLicensePayload);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.LicenseRevokedPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookLicensePayload** | [**WebhookLicensePayload**](WebhookLicensePayload.md) |  | [optional]  |

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
| **200** | Webhook processed successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="paymentcreatedpost"></a>
# **PaymentCreatedPost**
> void PaymentCreatedPost (WebhookPaymentPayload webhookPaymentPayload = null)

Payment Created

Occurs when a new payment is initiated (e.g., at checkout start or subscription creation). The payment may still be in an incomplete or pending state.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class PaymentCreatedPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DefaultApi(config);
            var webhookPaymentPayload = new WebhookPaymentPayload(); // WebhookPaymentPayload |  (optional) 

            try
            {
                // Payment Created
                apiInstance.PaymentCreatedPost(webhookPaymentPayload);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.PaymentCreatedPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PaymentCreatedPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Payment Created
    apiInstance.PaymentCreatedPostWithHttpInfo(webhookPaymentPayload);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.PaymentCreatedPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookPaymentPayload** | [**WebhookPaymentPayload**](WebhookPaymentPayload.md) |  | [optional]  |

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
| **200** | Webhook processed successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="paymentfailedpost"></a>
# **PaymentFailedPost**
> void PaymentFailedPost (Order order = null)

Payment Failed

Occurs when a customer payment attempt fails.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class PaymentFailedPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DefaultApi(config);
            var order = new Order(); // Order |  (optional) 

            try
            {
                // Payment Failed
                apiInstance.PaymentFailedPost(order);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.PaymentFailedPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PaymentFailedPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Payment Failed
    apiInstance.PaymentFailedPostWithHttpInfo(order);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.PaymentFailedPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **order** | [**Order**](Order.md) |  | [optional]  |

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
| **200** | Webhook processed successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="paymentsucceededpost"></a>
# **PaymentSucceededPost**
> void PaymentSucceededPost (Order order = null)

Payment Succeeded

Occurs when a customer payment is confirmed as succeeded.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class PaymentSucceededPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DefaultApi(config);
            var order = new Order(); // Order |  (optional) 

            try
            {
                // Payment Succeeded
                apiInstance.PaymentSucceededPost(order);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.PaymentSucceededPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PaymentSucceededPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Payment Succeeded
    apiInstance.PaymentSucceededPostWithHttpInfo(order);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.PaymentSucceededPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **order** | [**Order**](Order.md) |  | [optional]  |

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
| **200** | Webhook processed successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="refundfailedpost"></a>
# **RefundFailedPost**
> void RefundFailedPost (WebhookRefundPayload webhookRefundPayload = null)

Refund Failed

Occurs when a payment refund fails.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class RefundFailedPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DefaultApi(config);
            var webhookRefundPayload = new WebhookRefundPayload(); // WebhookRefundPayload |  (optional) 

            try
            {
                // Refund Failed
                apiInstance.RefundFailedPost(webhookRefundPayload);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.RefundFailedPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RefundFailedPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Refund Failed
    apiInstance.RefundFailedPostWithHttpInfo(webhookRefundPayload);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.RefundFailedPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookRefundPayload** | [**WebhookRefundPayload**](WebhookRefundPayload.md) |  | [optional]  |

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
| **200** | Webhook processed successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="refundsucceededpost"></a>
# **RefundSucceededPost**
> void RefundSucceededPost (WebhookRefundPayload webhookRefundPayload = null)

Refund Succeeded

Occurs when a payment refund is confirmed as succeeded.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class RefundSucceededPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DefaultApi(config);
            var webhookRefundPayload = new WebhookRefundPayload(); // WebhookRefundPayload |  (optional) 

            try
            {
                // Refund Succeeded
                apiInstance.RefundSucceededPost(webhookRefundPayload);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.RefundSucceededPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RefundSucceededPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Refund Succeeded
    apiInstance.RefundSucceededPostWithHttpInfo(webhookRefundPayload);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.RefundSucceededPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookRefundPayload** | [**WebhookRefundPayload**](WebhookRefundPayload.md) |  | [optional]  |

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
| **200** | Webhook processed successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="subscriptioncreatedpost"></a>
# **SubscriptionCreatedPost**
> void SubscriptionCreatedPost (WebhookSubscriptionPayload webhookSubscriptionPayload = null)

Subscription Created

Occurs when a customer subscription is successfully started.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class SubscriptionCreatedPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DefaultApi(config);
            var webhookSubscriptionPayload = new WebhookSubscriptionPayload(); // WebhookSubscriptionPayload |  (optional) 

            try
            {
                // Subscription Created
                apiInstance.SubscriptionCreatedPost(webhookSubscriptionPayload);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.SubscriptionCreatedPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SubscriptionCreatedPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Subscription Created
    apiInstance.SubscriptionCreatedPostWithHttpInfo(webhookSubscriptionPayload);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.SubscriptionCreatedPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookSubscriptionPayload** | [**WebhookSubscriptionPayload**](WebhookSubscriptionPayload.md) |  | [optional]  |

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
| **200** | Webhook processed successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="subscriptiondeactivatedpost"></a>
# **SubscriptionDeactivatedPost**
> void SubscriptionDeactivatedPost (WebhookSubscriptionPayload webhookSubscriptionPayload = null)

Subscription Deactivated

Occurs when a customer subscription is deactivated or expired.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class SubscriptionDeactivatedPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DefaultApi(config);
            var webhookSubscriptionPayload = new WebhookSubscriptionPayload(); // WebhookSubscriptionPayload |  (optional) 

            try
            {
                // Subscription Deactivated
                apiInstance.SubscriptionDeactivatedPost(webhookSubscriptionPayload);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.SubscriptionDeactivatedPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SubscriptionDeactivatedPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Subscription Deactivated
    apiInstance.SubscriptionDeactivatedPostWithHttpInfo(webhookSubscriptionPayload);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.SubscriptionDeactivatedPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookSubscriptionPayload** | [**WebhookSubscriptionPayload**](WebhookSubscriptionPayload.md) |  | [optional]  |

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
| **200** | Webhook processed successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="subscriptionupdatedpost"></a>
# **SubscriptionUpdatedPost**
> void SubscriptionUpdatedPost (WebhookSubscriptionPayload webhookSubscriptionPayload = null)

Subscription Updated

Occurs when a customer subscription is updated (e.g., cancel at period end changes).

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class SubscriptionUpdatedPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DefaultApi(config);
            var webhookSubscriptionPayload = new WebhookSubscriptionPayload(); // WebhookSubscriptionPayload |  (optional) 

            try
            {
                // Subscription Updated
                apiInstance.SubscriptionUpdatedPost(webhookSubscriptionPayload);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DefaultApi.SubscriptionUpdatedPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SubscriptionUpdatedPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Subscription Updated
    apiInstance.SubscriptionUpdatedPostWithHttpInfo(webhookSubscriptionPayload);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DefaultApi.SubscriptionUpdatedPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookSubscriptionPayload** | [**WebhookSubscriptionPayload**](WebhookSubscriptionPayload.md) |  | [optional]  |

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
| **200** | Webhook processed successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

