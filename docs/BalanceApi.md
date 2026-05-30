# Solifyn.Api.BalanceApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**BalanceControllerFindAll**](BalanceApi.md#balancecontrollerfindall) | **GET** /v1/balances |  |
| [**BalanceControllerGenerateReport**](BalanceApi.md#balancecontrollergeneratereport) | **GET** /v1/balances/report |  |
| [**BalanceControllerGetSummary**](BalanceApi.md#balancecontrollergetsummary) | **GET** /v1/balances/summary |  |

<a id="balancecontrollerfindall"></a>
# **BalanceControllerFindAll**
> void BalanceControllerFindAll ()



### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class BalanceControllerFindAllExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            var apiInstance = new BalanceApi(config);

            try
            {
                apiInstance.BalanceControllerFindAll();
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BalanceApi.BalanceControllerFindAll: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BalanceControllerFindAllWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.BalanceControllerFindAllWithHttpInfo();
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BalanceApi.BalanceControllerFindAllWithHttpInfo: " + e.Message);
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
| **200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="balancecontrollergeneratereport"></a>
# **BalanceControllerGenerateReport**
> void BalanceControllerGenerateReport ()



### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class BalanceControllerGenerateReportExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            var apiInstance = new BalanceApi(config);

            try
            {
                apiInstance.BalanceControllerGenerateReport();
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BalanceApi.BalanceControllerGenerateReport: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BalanceControllerGenerateReportWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.BalanceControllerGenerateReportWithHttpInfo();
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BalanceApi.BalanceControllerGenerateReportWithHttpInfo: " + e.Message);
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
| **200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="balancecontrollergetsummary"></a>
# **BalanceControllerGetSummary**
> void BalanceControllerGetSummary ()



### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class BalanceControllerGetSummaryExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            var apiInstance = new BalanceApi(config);

            try
            {
                apiInstance.BalanceControllerGetSummary();
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BalanceApi.BalanceControllerGetSummary: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BalanceControllerGetSummaryWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.BalanceControllerGetSummaryWithHttpInfo();
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BalanceApi.BalanceControllerGetSummaryWithHttpInfo: " + e.Message);
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
| **200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

