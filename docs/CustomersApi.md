# Solifyn.Api.CustomersApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CustomersCreate**](CustomersApi.md#customerscreate) | **POST** /v1/customers | Create Customer |
| [**CustomersGenerateInvite**](CustomersApi.md#customersgenerateinvite) | **POST** /v1/customers/{id}/share | Generate Shared Invite |
| [**CustomersGet**](CustomersApi.md#customersget) | **GET** /v1/customers/{id} | Retrieve Customer |
| [**CustomersList**](CustomersApi.md#customerslist) | **GET** /v1/customers | List Customers |
| [**CustomersUpdate**](CustomersApi.md#customersupdate) | **PATCH** /v1/customers/{id} | Update Customer |

<a id="customerscreate"></a>
# **CustomersCreate**
> CustomerResponseDto CustomersCreate (CreateCustomerDto createCustomerDto)

Create Customer

Add/upsert a new customer profile under the current business context.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class CustomersCreateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new CustomersApi(config);
            var createCustomerDto = new CreateCustomerDto(); // CreateCustomerDto | 

            try
            {
                // Create Customer
                CustomerResponseDto result = apiInstance.CustomersCreate(createCustomerDto);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CustomersApi.CustomersCreate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CustomersCreateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Customer
    ApiResponse<CustomerResponseDto> response = apiInstance.CustomersCreateWithHttpInfo(createCustomerDto);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CustomersApi.CustomersCreateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createCustomerDto** | [**CreateCustomerDto**](CreateCustomerDto.md) |  |  |

### Return type

[**CustomerResponseDto**](CustomerResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Customer created/updated successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="customersgenerateinvite"></a>
# **CustomersGenerateInvite**
> CustomerSharedInviteResponseDto CustomersGenerateInvite (string id)

Generate Shared Invite

Generate a short-lived token granting temporary customer self-service billing page access.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class CustomersGenerateInviteExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new CustomersApi(config);
            var id = user_123;  // string | Customer ID

            try
            {
                // Generate Shared Invite
                CustomerSharedInviteResponseDto result = apiInstance.CustomersGenerateInvite(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CustomersApi.CustomersGenerateInvite: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CustomersGenerateInviteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Generate Shared Invite
    ApiResponse<CustomerSharedInviteResponseDto> response = apiInstance.CustomersGenerateInviteWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CustomersApi.CustomersGenerateInviteWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | Customer ID |  |

### Return type

[**CustomerSharedInviteResponseDto**](CustomerSharedInviteResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Self-service billing portal invite token created. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="customersget"></a>
# **CustomersGet**
> CustomerResponseDto CustomersGet (string id)

Retrieve Customer

Retrieve details of a customer profile by ID.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class CustomersGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new CustomersApi(config);
            var id = user_123;  // string | Customer ID

            try
            {
                // Retrieve Customer
                CustomerResponseDto result = apiInstance.CustomersGet(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CustomersApi.CustomersGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CustomersGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieve Customer
    ApiResponse<CustomerResponseDto> response = apiInstance.CustomersGetWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CustomersApi.CustomersGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | Customer ID |  |

### Return type

[**CustomerResponseDto**](CustomerResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Customer details retrieved successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="customerslist"></a>
# **CustomersList**
> CustomerListResponseDto CustomersList ()

List Customers

Retrieve all customers associated with the current active business.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class CustomersListExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new CustomersApi(config);

            try
            {
                // List Customers
                CustomerListResponseDto result = apiInstance.CustomersList();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CustomersApi.CustomersList: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CustomersListWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Customers
    ApiResponse<CustomerListResponseDto> response = apiInstance.CustomersListWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CustomersApi.CustomersListWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**CustomerListResponseDto**](CustomerListResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | List of customers retrieved successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="customersupdate"></a>
# **CustomersUpdate**
> CustomerMessageResponseDto CustomersUpdate (string id, UpdateCustomerDto updateCustomerDto)

Update Customer

Update name, phone, or metadata of an existing customer profile.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class CustomersUpdateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new CustomersApi(config);
            var id = user_123;  // string | Customer ID
            var updateCustomerDto = new UpdateCustomerDto(); // UpdateCustomerDto | 

            try
            {
                // Update Customer
                CustomerMessageResponseDto result = apiInstance.CustomersUpdate(id, updateCustomerDto);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CustomersApi.CustomersUpdate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CustomersUpdateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Customer
    ApiResponse<CustomerMessageResponseDto> response = apiInstance.CustomersUpdateWithHttpInfo(id, updateCustomerDto);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CustomersApi.CustomersUpdateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | Customer ID |  |
| **updateCustomerDto** | [**UpdateCustomerDto**](UpdateCustomerDto.md) |  |  |

### Return type

[**CustomerMessageResponseDto**](CustomerMessageResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Customer updated successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

