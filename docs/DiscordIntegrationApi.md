# Solifyn.Api.DiscordIntegrationApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**DiscordGetInstallUrl**](DiscordIntegrationApi.md#discordgetinstallurl) | **GET** /v1/discord/install | Get Discord Bot Installation URL |
| [**DiscordListRoles**](DiscordIntegrationApi.md#discordlistroles) | **GET** /v1/discord/roles | List Guild Discord Roles |

<a id="discordgetinstallurl"></a>
# **DiscordGetInstallUrl**
> void DiscordGetInstallUrl (string productId = null)

Get Discord Bot Installation URL

Generates the URL to invite the system-wide Discord Bot onto the merchant's Discord server.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class DiscordGetInstallUrlExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            var apiInstance = new DiscordIntegrationApi(config);
            var productId = "productId_example";  // string | Optional Product ID to redirect back to after installation (optional) 

            try
            {
                // Get Discord Bot Installation URL
                apiInstance.DiscordGetInstallUrl(productId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DiscordIntegrationApi.DiscordGetInstallUrl: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DiscordGetInstallUrlWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Discord Bot Installation URL
    apiInstance.DiscordGetInstallUrlWithHttpInfo(productId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DiscordIntegrationApi.DiscordGetInstallUrlWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **productId** | **string** | Optional Product ID to redirect back to after installation | [optional]  |

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
| **200** | Returns the generated installation URL. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="discordlistroles"></a>
# **DiscordListRoles**
> List&lt;DiscordRolesResponseDto&gt; DiscordListRoles ()

List Guild Discord Roles

Retrieves all roles available in the connected merchant's Discord server/guild.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class DiscordListRolesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            var apiInstance = new DiscordIntegrationApi(config);

            try
            {
                // List Guild Discord Roles
                List<DiscordRolesResponseDto> result = apiInstance.DiscordListRoles();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DiscordIntegrationApi.DiscordListRoles: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DiscordListRolesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Guild Discord Roles
    ApiResponse<List<DiscordRolesResponseDto>> response = apiInstance.DiscordListRolesWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DiscordIntegrationApi.DiscordListRolesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**List&lt;DiscordRolesResponseDto&gt;**](DiscordRolesResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | List of server roles. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

