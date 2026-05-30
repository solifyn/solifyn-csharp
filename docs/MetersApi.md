# Solifyn.Api.MetersApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**EventsIngest**](MetersApi.md#eventsingest) | **POST** /v1/meters/ingest | Ingest Events |
| [**MetersCreate**](MetersApi.md#meterscreate) | **POST** /v1/meters | Create Meter |
| [**MetersGet**](MetersApi.md#metersget) | **GET** /v1/meters/{id} | Retrieve Meter |
| [**MetersGetEvents**](MetersApi.md#metersgetevents) | **GET** /v1/meters/{id}/events | List Meter Events |
| [**MetersGetQuantities**](MetersApi.md#metersgetquantities) | **GET** /v1/meters/{id}/quantities | Get Meter Quantities |
| [**MetersList**](MetersApi.md#meterslist) | **GET** /v1/meters | List Meters |
| [**MetersUpdate**](MetersApi.md#metersupdate) | **PATCH** /v1/meters/{id} | Update Meter |

<a id="eventsingest"></a>
# **EventsIngest**
> MeterIngestResponseDto EventsIngest (MeterIngestRequestDto meterIngestRequestDto)

Ingest Events

Ingest usage events for meters.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class EventsIngestExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new MetersApi(config);
            var meterIngestRequestDto = new MeterIngestRequestDto(); // MeterIngestRequestDto | 

            try
            {
                // Ingest Events
                MeterIngestResponseDto result = apiInstance.EventsIngest(meterIngestRequestDto);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MetersApi.EventsIngest: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EventsIngestWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Ingest Events
    ApiResponse<MeterIngestResponseDto> response = apiInstance.EventsIngestWithHttpInfo(meterIngestRequestDto);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MetersApi.EventsIngestWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **meterIngestRequestDto** | [**MeterIngestRequestDto**](MeterIngestRequestDto.md) |  |  |

### Return type

[**MeterIngestResponseDto**](MeterIngestResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Events ingested successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="meterscreate"></a>
# **MetersCreate**
> MeterResponseDto MetersCreate (CreateMeterDto createMeterDto)

Create Meter

Create a new usage meter for event-based billing and usage tracking.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class MetersCreateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new MetersApi(config);
            var createMeterDto = new CreateMeterDto(); // CreateMeterDto | 

            try
            {
                // Create Meter
                MeterResponseDto result = apiInstance.MetersCreate(createMeterDto);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MetersApi.MetersCreate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the MetersCreateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Meter
    ApiResponse<MeterResponseDto> response = apiInstance.MetersCreateWithHttpInfo(createMeterDto);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MetersApi.MetersCreateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createMeterDto** | [**CreateMeterDto**](CreateMeterDto.md) |  |  |

### Return type

[**MeterResponseDto**](MeterResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Meter created successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="metersget"></a>
# **MetersGet**
> MeterDetailResponseDto MetersGet (string id, string startDate, string endDate)

Retrieve Meter

Retrieve a meter and its most recent usage events.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class MetersGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new MetersApi(config);
            var id = mtr_8Z1aB2cD3eF4gH5iJ6kL7m;  // string | The unique meter ID.
            var startDate = "startDate_example";  // string | 
            var endDate = "endDate_example";  // string | 

            try
            {
                // Retrieve Meter
                MeterDetailResponseDto result = apiInstance.MetersGet(id, startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MetersApi.MetersGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the MetersGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieve Meter
    ApiResponse<MeterDetailResponseDto> response = apiInstance.MetersGetWithHttpInfo(id, startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MetersApi.MetersGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The unique meter ID. |  |
| **startDate** | **string** |  |  |
| **endDate** | **string** |  |  |

### Return type

[**MeterDetailResponseDto**](MeterDetailResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Meter retrieved successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="metersgetevents"></a>
# **MetersGetEvents**
> MeterEventsResponseDto MetersGetEvents (string id, decimal? limit = null)

List Meter Events

List recent usage events recorded for a meter.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class MetersGetEventsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new MetersApi(config);
            var id = mtr_8Z1aB2cD3eF4gH5iJ6kL7m;  // string | The unique meter ID.
            var limit = 100MD;  // decimal? | Maximum number of usage events to return. (optional)  (default to 100M)

            try
            {
                // List Meter Events
                MeterEventsResponseDto result = apiInstance.MetersGetEvents(id, limit);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MetersApi.MetersGetEvents: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the MetersGetEventsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Meter Events
    ApiResponse<MeterEventsResponseDto> response = apiInstance.MetersGetEventsWithHttpInfo(id, limit);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MetersApi.MetersGetEventsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The unique meter ID. |  |
| **limit** | **decimal?** | Maximum number of usage events to return. | [optional] [default to 100M] |

### Return type

[**MeterEventsResponseDto**](MeterEventsResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Meter events retrieved successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="metersgetquantities"></a>
# **MetersGetQuantities**
> MeterQuantitiesResponseDto MetersGetQuantities (string id, string startDate = null, string endDate = null)

Get Meter Quantities

Get aggregated usage quantities for a meter within an optional date range.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class MetersGetQuantitiesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new MetersApi(config);
            var id = mtr_8Z1aB2cD3eF4gH5iJ6kL7m;  // string | The unique meter ID.
            var startDate = "startDate_example";  // string | Inclusive start date in ISO 8601 format. (optional) 
            var endDate = "endDate_example";  // string | Inclusive end date in ISO 8601 format. (optional) 

            try
            {
                // Get Meter Quantities
                MeterQuantitiesResponseDto result = apiInstance.MetersGetQuantities(id, startDate, endDate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MetersApi.MetersGetQuantities: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the MetersGetQuantitiesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Meter Quantities
    ApiResponse<MeterQuantitiesResponseDto> response = apiInstance.MetersGetQuantitiesWithHttpInfo(id, startDate, endDate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MetersApi.MetersGetQuantitiesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The unique meter ID. |  |
| **startDate** | **string** | Inclusive start date in ISO 8601 format. | [optional]  |
| **endDate** | **string** | Inclusive end date in ISO 8601 format. | [optional]  |

### Return type

[**MeterQuantitiesResponseDto**](MeterQuantitiesResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Meter quantities retrieved successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="meterslist"></a>
# **MetersList**
> List&lt;MeterResponseDto&gt; MetersList (string status = null)

List Meters

List meters belonging to your active business. You can filter by archived status.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class MetersListExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new MetersApi(config);
            var status = "active";  // string | Filter by meter status. (optional) 

            try
            {
                // List Meters
                List<MeterResponseDto> result = apiInstance.MetersList(status);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MetersApi.MetersList: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the MetersListWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Meters
    ApiResponse<List<MeterResponseDto>> response = apiInstance.MetersListWithHttpInfo(status);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MetersApi.MetersListWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **status** | **string** | Filter by meter status. | [optional]  |

### Return type

[**List&lt;MeterResponseDto&gt;**](MeterResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Meters retrieved successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="metersupdate"></a>
# **MetersUpdate**
> MeterResponseDto MetersUpdate (string id, UpdateMeterDto updateMeterDto)

Update Meter

Update an existing meter definition.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class MetersUpdateExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new MetersApi(config);
            var id = mtr_8Z1aB2cD3eF4gH5iJ6kL7m;  // string | The unique meter ID.
            var updateMeterDto = new UpdateMeterDto(); // UpdateMeterDto | 

            try
            {
                // Update Meter
                MeterResponseDto result = apiInstance.MetersUpdate(id, updateMeterDto);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MetersApi.MetersUpdate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the MetersUpdateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Meter
    ApiResponse<MeterResponseDto> response = apiInstance.MetersUpdateWithHttpInfo(id, updateMeterDto);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MetersApi.MetersUpdateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The unique meter ID. |  |
| **updateMeterDto** | [**UpdateMeterDto**](UpdateMeterDto.md) |  |  |

### Return type

[**MeterResponseDto**](MeterResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Meter updated successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

