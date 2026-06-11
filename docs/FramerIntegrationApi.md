# Solifyn.Api.FramerIntegrationApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**FramerCreateTemplate**](FramerIntegrationApi.md#framercreatetemplate) | **POST** /v1/framer/templates | Create Framer Template |
| [**FramerDeleteTemplate**](FramerIntegrationApi.md#framerdeletetemplate) | **DELETE** /v1/framer/templates/{id} | Delete Framer Template |
| [**FramerGetTemplate**](FramerIntegrationApi.md#framergettemplate) | **GET** /v1/framer/templates/{id} | Retrieve Framer Template |
| [**FramerListTemplates**](FramerIntegrationApi.md#framerlisttemplates) | **GET** /v1/framer/templates | List Framer Templates |
| [**FramerUpdateTemplate**](FramerIntegrationApi.md#framerupdatetemplate) | **PUT** /v1/framer/templates/{id} | Update Framer Template |

<a id="framercreatetemplate"></a>
# **FramerCreateTemplate**
> FramerTemplateResponseDto FramerCreateTemplate (CreateFramerTemplateDto createFramerTemplateDto)

Create Framer Template

Registers a new Framer template with its public remix link for the active business.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class FramerCreateTemplateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new FramerIntegrationApi(config);
            var createFramerTemplateDto = new CreateFramerTemplateDto(); // CreateFramerTemplateDto | 

            try
            {
                // Create Framer Template
                FramerTemplateResponseDto result = apiInstance.FramerCreateTemplate(createFramerTemplateDto);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FramerIntegrationApi.FramerCreateTemplate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FramerCreateTemplateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Framer Template
    ApiResponse<FramerTemplateResponseDto> response = apiInstance.FramerCreateTemplateWithHttpInfo(createFramerTemplateDto);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FramerIntegrationApi.FramerCreateTemplateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createFramerTemplateDto** | [**CreateFramerTemplateDto**](CreateFramerTemplateDto.md) |  |  |

### Return type

[**FramerTemplateResponseDto**](FramerTemplateResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Template created successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="framerdeletetemplate"></a>
# **FramerDeleteTemplate**
> void FramerDeleteTemplate (string id)

Delete Framer Template

Deletes a registered Framer template for the active business.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class FramerDeleteTemplateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new FramerIntegrationApi(config);
            var id = "id_example";  // string | The Framer template ID

            try
            {
                // Delete Framer Template
                apiInstance.FramerDeleteTemplate(id);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FramerIntegrationApi.FramerDeleteTemplate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FramerDeleteTemplateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete Framer Template
    apiInstance.FramerDeleteTemplateWithHttpInfo(id);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FramerIntegrationApi.FramerDeleteTemplateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The Framer template ID |  |

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Template deleted successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="framergettemplate"></a>
# **FramerGetTemplate**
> FramerTemplateResponseDto FramerGetTemplate (string id)

Retrieve Framer Template

Retrieves details of a specific registered Framer template.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class FramerGetTemplateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new FramerIntegrationApi(config);
            var id = "id_example";  // string | The Framer template ID

            try
            {
                // Retrieve Framer Template
                FramerTemplateResponseDto result = apiInstance.FramerGetTemplate(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FramerIntegrationApi.FramerGetTemplate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FramerGetTemplateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieve Framer Template
    ApiResponse<FramerTemplateResponseDto> response = apiInstance.FramerGetTemplateWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FramerIntegrationApi.FramerGetTemplateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The Framer template ID |  |

### Return type

[**FramerTemplateResponseDto**](FramerTemplateResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Details of the Framer template. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="framerlisttemplates"></a>
# **FramerListTemplates**
> List&lt;FramerTemplateResponseDto&gt; FramerListTemplates ()

List Framer Templates

Retrieves all registered Framer templates for the active business.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class FramerListTemplatesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new FramerIntegrationApi(config);

            try
            {
                // List Framer Templates
                List<FramerTemplateResponseDto> result = apiInstance.FramerListTemplates();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FramerIntegrationApi.FramerListTemplates: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FramerListTemplatesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Framer Templates
    ApiResponse<List<FramerTemplateResponseDto>> response = apiInstance.FramerListTemplatesWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FramerIntegrationApi.FramerListTemplatesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**List&lt;FramerTemplateResponseDto&gt;**](FramerTemplateResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | List of Framer templates. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="framerupdatetemplate"></a>
# **FramerUpdateTemplate**
> FramerTemplateResponseDto FramerUpdateTemplate (string id, UpdateFramerTemplateDto updateFramerTemplateDto)

Update Framer Template

Updates a registered Framer template for the active business.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class FramerUpdateTemplateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new FramerIntegrationApi(config);
            var id = "id_example";  // string | The Framer template ID
            var updateFramerTemplateDto = new UpdateFramerTemplateDto(); // UpdateFramerTemplateDto | 

            try
            {
                // Update Framer Template
                FramerTemplateResponseDto result = apiInstance.FramerUpdateTemplate(id, updateFramerTemplateDto);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FramerIntegrationApi.FramerUpdateTemplate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FramerUpdateTemplateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Framer Template
    ApiResponse<FramerTemplateResponseDto> response = apiInstance.FramerUpdateTemplateWithHttpInfo(id, updateFramerTemplateDto);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FramerIntegrationApi.FramerUpdateTemplateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The Framer template ID |  |
| **updateFramerTemplateDto** | [**UpdateFramerTemplateDto**](UpdateFramerTemplateDto.md) |  |  |

### Return type

[**FramerTemplateResponseDto**](FramerTemplateResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Template updated successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

