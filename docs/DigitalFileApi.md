# Solifyn.Api.DigitalFileApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**DigitalFileControllerCreate**](DigitalFileApi.md#digitalfilecontrollercreate) | **POST** /v1/digital-files |  |
| [**DigitalFileControllerFindAll**](DigitalFileApi.md#digitalfilecontrollerfindall) | **GET** /v1/digital-files |  |
| [**DigitalFileControllerRemove**](DigitalFileApi.md#digitalfilecontrollerremove) | **DELETE** /v1/digital-files/{id} |  |

<a id="digitalfilecontrollercreate"></a>
# **DigitalFileControllerCreate**
> void DigitalFileControllerCreate ()



### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class DigitalFileControllerCreateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            var apiInstance = new DigitalFileApi(config);

            try
            {
                apiInstance.DigitalFileControllerCreate();
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DigitalFileApi.DigitalFileControllerCreate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DigitalFileControllerCreateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.DigitalFileControllerCreateWithHttpInfo();
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DigitalFileApi.DigitalFileControllerCreateWithHttpInfo: " + e.Message);
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

<a id="digitalfilecontrollerfindall"></a>
# **DigitalFileControllerFindAll**
> void DigitalFileControllerFindAll ()



### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class DigitalFileControllerFindAllExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            var apiInstance = new DigitalFileApi(config);

            try
            {
                apiInstance.DigitalFileControllerFindAll();
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DigitalFileApi.DigitalFileControllerFindAll: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DigitalFileControllerFindAllWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.DigitalFileControllerFindAllWithHttpInfo();
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DigitalFileApi.DigitalFileControllerFindAllWithHttpInfo: " + e.Message);
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

<a id="digitalfilecontrollerremove"></a>
# **DigitalFileControllerRemove**
> void DigitalFileControllerRemove (string id)



### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class DigitalFileControllerRemoveExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            var apiInstance = new DigitalFileApi(config);
            var id = "id_example";  // string | 

            try
            {
                apiInstance.DigitalFileControllerRemove(id);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DigitalFileApi.DigitalFileControllerRemove: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DigitalFileControllerRemoveWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    apiInstance.DigitalFileControllerRemoveWithHttpInfo(id);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DigitalFileApi.DigitalFileControllerRemoveWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** |  |  |

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

