# Solifyn.Api.PayoutsApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**PayoutsCreateWithdrawal**](PayoutsApi.md#payoutscreatewithdrawal) | **POST** /v1/payouts/withdrawals | Create Withdrawal |
| [**PayoutsGetAccount**](PayoutsApi.md#payoutsgetaccount) | **GET** /v1/payouts/account | Retrieve Payout Account |
| [**PayoutsGetAccountLink**](PayoutsApi.md#payoutsgetaccountlink) | **GET** /v1/payouts/account-link | Create Account Link |
| [**PayoutsGetToken**](PayoutsApi.md#payoutsgettoken) | **GET** /v1/payouts/token | Generate Portal Access Token |
| [**PayoutsGetWithdrawals**](PayoutsApi.md#payoutsgetwithdrawals) | **GET** /v1/payouts/withdrawals | Get Withdrawals List |
| [**PayoutsListMethods**](PayoutsApi.md#payoutslistmethods) | **GET** /v1/payouts/methods | List Payout Methods |
| [**PayoutsListVerifications**](PayoutsApi.md#payoutslistverifications) | **GET** /v1/payouts/verifications | List Verifications |
| [**PayoutsListWithdrawals**](PayoutsApi.md#payoutslistwithdrawals) | **GET** /v1/payouts | List Withdrawals |

<a id="payoutscreatewithdrawal"></a>
# **PayoutsCreateWithdrawal**
> Withdrawal PayoutsCreateWithdrawal (WithdrawalCreate withdrawalCreate)

Create Withdrawal

Initiate a balance withdrawal transfer request.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class PayoutsCreateWithdrawalExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new PayoutsApi(config);
            var withdrawalCreate = new WithdrawalCreate(); // WithdrawalCreate | 

            try
            {
                // Create Withdrawal
                Withdrawal result = apiInstance.PayoutsCreateWithdrawal(withdrawalCreate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PayoutsApi.PayoutsCreateWithdrawal: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PayoutsCreateWithdrawalWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Withdrawal
    ApiResponse<Withdrawal> response = apiInstance.PayoutsCreateWithdrawalWithHttpInfo(withdrawalCreate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PayoutsApi.PayoutsCreateWithdrawalWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **withdrawalCreate** | [**WithdrawalCreate**](WithdrawalCreate.md) |  |  |

### Return type

[**Withdrawal**](Withdrawal.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Withdrawal successfully initiated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="payoutsgetaccount"></a>
# **PayoutsGetAccount**
> PayoutAccount PayoutsGetAccount ()

Retrieve Payout Account

Retrieve general status and information of onboarding payout accounts.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class PayoutsGetAccountExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new PayoutsApi(config);

            try
            {
                // Retrieve Payout Account
                PayoutAccount result = apiInstance.PayoutsGetAccount();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PayoutsApi.PayoutsGetAccount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PayoutsGetAccountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieve Payout Account
    ApiResponse<PayoutAccount> response = apiInstance.PayoutsGetAccountWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PayoutsApi.PayoutsGetAccountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**PayoutAccount**](PayoutAccount.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Payout account details retrieved successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="payoutsgetaccountlink"></a>
# **PayoutsGetAccountLink**
> PayoutAccountLink PayoutsGetAccountLink (string useCase = null)

Create Account Link

Generate temporary links for onboarding or viewing portals.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class PayoutsGetAccountLinkExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new PayoutsApi(config);
            var useCase = "account_onboarding";  // string | Onboarding link type context (optional) 

            try
            {
                // Create Account Link
                PayoutAccountLink result = apiInstance.PayoutsGetAccountLink(useCase);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PayoutsApi.PayoutsGetAccountLink: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PayoutsGetAccountLinkWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Account Link
    ApiResponse<PayoutAccountLink> response = apiInstance.PayoutsGetAccountLinkWithHttpInfo(useCase);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PayoutsApi.PayoutsGetAccountLinkWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **useCase** | **string** | Onboarding link type context | [optional]  |

### Return type

[**PayoutAccountLink**](PayoutAccountLink.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Account connection link generated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="payoutsgettoken"></a>
# **PayoutsGetToken**
> PayoutAccessToken PayoutsGetToken ()

Generate Portal Access Token

Generate temporary credentials to access the embed portal.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class PayoutsGetTokenExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new PayoutsApi(config);

            try
            {
                // Generate Portal Access Token
                PayoutAccessToken result = apiInstance.PayoutsGetToken();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PayoutsApi.PayoutsGetToken: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PayoutsGetTokenWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Generate Portal Access Token
    ApiResponse<PayoutAccessToken> response = apiInstance.PayoutsGetTokenWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PayoutsApi.PayoutsGetTokenWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**PayoutAccessToken**](PayoutAccessToken.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Portal access token successfully generated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="payoutsgetwithdrawals"></a>
# **PayoutsGetWithdrawals**
> WithdrawalList PayoutsGetWithdrawals (decimal? limit = null, decimal? page = null)

Get Withdrawals List

Retrieve withdrawal records for the active business.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class PayoutsGetWithdrawalsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new PayoutsApi(config);
            var limit = 8.14D;  // decimal? | Page size limit (optional) 
            var page = 8.14D;  // decimal? | Page number (optional) 

            try
            {
                // Get Withdrawals List
                WithdrawalList result = apiInstance.PayoutsGetWithdrawals(limit, page);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PayoutsApi.PayoutsGetWithdrawals: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PayoutsGetWithdrawalsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Withdrawals List
    ApiResponse<WithdrawalList> response = apiInstance.PayoutsGetWithdrawalsWithHttpInfo(limit, page);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PayoutsApi.PayoutsGetWithdrawalsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **limit** | **decimal?** | Page size limit | [optional]  |
| **page** | **decimal?** | Page number | [optional]  |

### Return type

[**WithdrawalList**](WithdrawalList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Withdrawals list retrieved successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="payoutslistmethods"></a>
# **PayoutsListMethods**
> PayoutMethodList PayoutsListMethods (decimal? limit = null, decimal? page = null)

List Payout Methods

List saved payout destinations (bank accounts, cards).

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class PayoutsListMethodsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new PayoutsApi(config);
            var limit = 8.14D;  // decimal? |  (optional) 
            var page = 8.14D;  // decimal? |  (optional) 

            try
            {
                // List Payout Methods
                PayoutMethodList result = apiInstance.PayoutsListMethods(limit, page);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PayoutsApi.PayoutsListMethods: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PayoutsListMethodsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Payout Methods
    ApiResponse<PayoutMethodList> response = apiInstance.PayoutsListMethodsWithHttpInfo(limit, page);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PayoutsApi.PayoutsListMethodsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **limit** | **decimal?** |  | [optional]  |
| **page** | **decimal?** |  | [optional]  |

### Return type

[**PayoutMethodList**](PayoutMethodList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Payout methods retrieved successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="payoutslistverifications"></a>
# **PayoutsListVerifications**
> PayoutVerificationList PayoutsListVerifications (decimal? limit = null, decimal? page = null)

List Verifications

Retrieve pending or completed KYC verification checks.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class PayoutsListVerificationsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new PayoutsApi(config);
            var limit = 8.14D;  // decimal? |  (optional) 
            var page = 8.14D;  // decimal? |  (optional) 

            try
            {
                // List Verifications
                PayoutVerificationList result = apiInstance.PayoutsListVerifications(limit, page);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PayoutsApi.PayoutsListVerifications: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PayoutsListVerificationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Verifications
    ApiResponse<PayoutVerificationList> response = apiInstance.PayoutsListVerificationsWithHttpInfo(limit, page);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PayoutsApi.PayoutsListVerificationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **limit** | **decimal?** |  | [optional]  |
| **page** | **decimal?** |  | [optional]  |

### Return type

[**PayoutVerificationList**](PayoutVerificationList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | KYC verifications list retrieved. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="payoutslistwithdrawals"></a>
# **PayoutsListWithdrawals**
> WithdrawalList PayoutsListWithdrawals (decimal? limit = null, decimal? page = null)

List Withdrawals

Retrieve a list of past withdrawal history.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class PayoutsListWithdrawalsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new PayoutsApi(config);
            var limit = 8.14D;  // decimal? | Page size limit (optional) 
            var page = 8.14D;  // decimal? | Page number (optional) 

            try
            {
                // List Withdrawals
                WithdrawalList result = apiInstance.PayoutsListWithdrawals(limit, page);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PayoutsApi.PayoutsListWithdrawals: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PayoutsListWithdrawalsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Withdrawals
    ApiResponse<WithdrawalList> response = apiInstance.PayoutsListWithdrawalsWithHttpInfo(limit, page);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PayoutsApi.PayoutsListWithdrawalsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **limit** | **decimal?** | Page size limit | [optional]  |
| **page** | **decimal?** | Page number | [optional]  |

### Return type

[**WithdrawalList**](WithdrawalList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Withdrawals list retrieved successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

