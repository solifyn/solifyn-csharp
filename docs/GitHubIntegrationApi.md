# Solifyn.Api.GitHubIntegrationApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GithubGetInstallUrl**](GitHubIntegrationApi.md#githubgetinstallurl) | **GET** /v1/github/install | Get GitHub App Installation URL |
| [**GithubListRepos**](GitHubIntegrationApi.md#githublistrepos) | **GET** /v1/github/repos | List Available GitHub Repositories |

<a id="githubgetinstallurl"></a>
# **GithubGetInstallUrl**
> void GithubGetInstallUrl (string productId = null)

Get GitHub App Installation URL

Generates the URL to install the system-wide GitHub App onto the merchant's GitHub account/org.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class GithubGetInstallUrlExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new GitHubIntegrationApi(config);
            var productId = "productId_example";  // string | Optional Product ID to redirect back to after installation (optional) 

            try
            {
                // Get GitHub App Installation URL
                apiInstance.GithubGetInstallUrl(productId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GitHubIntegrationApi.GithubGetInstallUrl: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GithubGetInstallUrlWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get GitHub App Installation URL
    apiInstance.GithubGetInstallUrlWithHttpInfo(productId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GitHubIntegrationApi.GithubGetInstallUrlWithHttpInfo: " + e.Message);
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

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Returns the generated installation URL. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="githublistrepos"></a>
# **GithubListRepos**
> List&lt;GithubReposResponseDto&gt; GithubListRepos ()

List Available GitHub Repositories

Retrieves all repositories accessible by the merchant's installed GitHub App.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class GithubListReposExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.solifyn.com";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new GitHubIntegrationApi(config);

            try
            {
                // List Available GitHub Repositories
                List<GithubReposResponseDto> result = apiInstance.GithubListRepos();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GitHubIntegrationApi.GithubListRepos: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GithubListReposWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Available GitHub Repositories
    ApiResponse<List<GithubReposResponseDto>> response = apiInstance.GithubListReposWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GitHubIntegrationApi.GithubListReposWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**List&lt;GithubReposResponseDto&gt;**](GithubReposResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | List of repositories. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

