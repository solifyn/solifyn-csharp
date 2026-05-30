# Solifyn.Api.DisputesApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**DisputesGenerateReport**](DisputesApi.md#disputesgeneratereport) | **GET** /v1/transactions/disputes/report | Generate Dispute CSV Report |
| [**DisputesGet**](DisputesApi.md#disputesget) | **GET** /v1/transactions/disputes/{id} | Retrieve Dispute |
| [**DisputesList**](DisputesApi.md#disputeslist) | **GET** /v1/transactions/disputes | List Disputes |
| [**DisputesSubmitEvidence**](DisputesApi.md#disputessubmitevidence) | **POST** /v1/transactions/disputes/{id}/submit | Submit Dispute Evidence |
| [**DisputesUpdateEvidence**](DisputesApi.md#disputesupdateevidence) | **PATCH** /v1/transactions/disputes/{id}/evidence | Update Dispute Evidence |
| [**DisputesUploadEvidenceFile**](DisputesApi.md#disputesuploadevidencefile) | **POST** /v1/transactions/disputes/upload | Upload Evidence File |

<a id="disputesgeneratereport"></a>
# **DisputesGenerateReport**
> void DisputesGenerateReport (string createdAtGte = null, string createdAtLte = null, string status = null)

Generate Dispute CSV Report

Generates a downloadable CSV report of disputes matching the filters.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class DisputesGenerateReportExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DisputesApi(config);
            var createdAtGte = "createdAtGte_example";  // string | Filter disputes created after this ISO date-time string (optional) 
            var createdAtLte = "createdAtLte_example";  // string | Filter disputes created before this ISO date-time string (optional) 
            var status = "status_example";  // string | Filter disputes by status (optional) 

            try
            {
                // Generate Dispute CSV Report
                apiInstance.DisputesGenerateReport(createdAtGte, createdAtLte, status);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DisputesApi.DisputesGenerateReport: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DisputesGenerateReportWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Generate Dispute CSV Report
    apiInstance.DisputesGenerateReportWithHttpInfo(createdAtGte, createdAtLte, status);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DisputesApi.DisputesGenerateReportWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createdAtGte** | **string** | Filter disputes created after this ISO date-time string | [optional]  |
| **createdAtLte** | **string** | Filter disputes created before this ISO date-time string | [optional]  |
| **status** | **string** | Filter disputes by status | [optional]  |

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
| **200** | CSV report file contents generated successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="disputesget"></a>
# **DisputesGet**
> Dispute DisputesGet (string id)

Retrieve Dispute

Retrieve details of a specific dispute by ID.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class DisputesGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DisputesApi(config);
            var id = dsp_123;  // string | The dispute ID

            try
            {
                // Retrieve Dispute
                Dispute result = apiInstance.DisputesGet(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DisputesApi.DisputesGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DisputesGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieve Dispute
    ApiResponse<Dispute> response = apiInstance.DisputesGetWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DisputesApi.DisputesGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The dispute ID |  |

### Return type

[**Dispute**](Dispute.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Dispute details retrieved successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="disputeslist"></a>
# **DisputesList**
> DisputeList DisputesList (string page = null, string limit = null, string status = null, string type = null)

List Disputes

Retrieve disputes associated with the active business.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class DisputesListExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DisputesApi(config);
            var page = 1;  // string | Page number for pagination (optional) 
            var limit = 10;  // string | Page size limit for pagination (optional) 
            var status = "status_example";  // string | Filter disputes by status (optional) 
            var type = "type_example";  // string | Filter by type: dispute or alert (optional) 

            try
            {
                // List Disputes
                DisputeList result = apiInstance.DisputesList(page, limit, status, type);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DisputesApi.DisputesList: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DisputesListWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Disputes
    ApiResponse<DisputeList> response = apiInstance.DisputesListWithHttpInfo(page, limit, status, type);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DisputesApi.DisputesListWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **page** | **string** | Page number for pagination | [optional]  |
| **limit** | **string** | Page size limit for pagination | [optional]  |
| **status** | **string** | Filter disputes by status | [optional]  |
| **type** | **string** | Filter by type: dispute or alert | [optional]  |

### Return type

[**DisputeList**](DisputeList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Dispute list retrieved successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="disputessubmitevidence"></a>
# **DisputesSubmitEvidence**
> Dispute DisputesSubmitEvidence (string id)

Submit Dispute Evidence

Finalize and submit the uploaded evidence for review.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class DisputesSubmitEvidenceExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DisputesApi(config);
            var id = dsp_123;  // string | The dispute ID

            try
            {
                // Submit Dispute Evidence
                Dispute result = apiInstance.DisputesSubmitEvidence(id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DisputesApi.DisputesSubmitEvidence: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DisputesSubmitEvidenceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Submit Dispute Evidence
    ApiResponse<Dispute> response = apiInstance.DisputesSubmitEvidenceWithHttpInfo(id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DisputesApi.DisputesSubmitEvidenceWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The dispute ID |  |

### Return type

[**Dispute**](Dispute.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Dispute evidence successfully submitted. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="disputesupdateevidence"></a>
# **DisputesUpdateEvidence**
> Dispute DisputesUpdateEvidence (string id, DisputeEvidenceUpdate disputeEvidenceUpdate)

Update Dispute Evidence

Upload and update evidence attachments for a dispute.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class DisputesUpdateEvidenceExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DisputesApi(config);
            var id = dsp_123;  // string | The dispute ID
            var disputeEvidenceUpdate = new DisputeEvidenceUpdate(); // DisputeEvidenceUpdate | 

            try
            {
                // Update Dispute Evidence
                Dispute result = apiInstance.DisputesUpdateEvidence(id, disputeEvidenceUpdate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DisputesApi.DisputesUpdateEvidence: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DisputesUpdateEvidenceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Dispute Evidence
    ApiResponse<Dispute> response = apiInstance.DisputesUpdateEvidenceWithHttpInfo(id, disputeEvidenceUpdate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DisputesApi.DisputesUpdateEvidenceWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The dispute ID |  |
| **disputeEvidenceUpdate** | [**DisputeEvidenceUpdate**](DisputeEvidenceUpdate.md) |  |  |

### Return type

[**Dispute**](Dispute.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Dispute evidence successfully updated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="disputesuploadevidencefile"></a>
# **DisputesUploadEvidenceFile**
> DisputeFileUpload DisputesUploadEvidenceFile (System.IO.Stream file)

Upload Evidence File

Upload a support file (image, PDF, video) to use as dispute evidence.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class DisputesUploadEvidenceFileExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            // Configure Bearer token for authorization: ApiKeyAuth
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DisputesApi(config);
            var file = new System.IO.MemoryStream(System.IO.File.ReadAllBytes("/path/to/file.txt"));  // System.IO.Stream | The evidence file to upload (Max 25MB: JPEG, PNG, GIF, WEBP, PDF, MP4, WEBM, QuickTime)

            try
            {
                // Upload Evidence File
                DisputeFileUpload result = apiInstance.DisputesUploadEvidenceFile(file);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DisputesApi.DisputesUploadEvidenceFile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DisputesUploadEvidenceFileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Upload Evidence File
    ApiResponse<DisputeFileUpload> response = apiInstance.DisputesUploadEvidenceFileWithHttpInfo(file);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DisputesApi.DisputesUploadEvidenceFileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **file** | **System.IO.Stream****System.IO.Stream** | The evidence file to upload (Max 25MB: JPEG, PNG, GIF, WEBP, PDF, MP4, WEBM, QuickTime) |  |

### Return type

[**DisputeFileUpload**](DisputeFileUpload.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | File upload details successfully created. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

