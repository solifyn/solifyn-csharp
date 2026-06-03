# Solifyn.Api.RefundRequestsApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**RefundRequestsList**](RefundRequestsApi.md#refundrequestslist) | **GET** /v1/refund-requests | List Refund Requests (Merchant) |
| [**RefundRequestsListMessages**](RefundRequestsApi.md#refundrequestslistmessages) | **GET** /v1/refund-requests/{id}/messages | List Messages for Refund Request (Merchant) |
| [**RefundRequestsSendMessage**](RefundRequestsApi.md#refundrequestssendmessage) | **POST** /v1/refund-requests/{id}/messages | Send Refund Request Message (Merchant) |
| [**RefundRequestsUpdateStatus**](RefundRequestsApi.md#refundrequestsupdatestatus) | **PATCH** /v1/refund-requests/{id}/status | Update Refund Request Status (Merchant) |
| [**RefundRequestsUploadEvidence**](RefundRequestsApi.md#refundrequestsuploadevidence) | **POST** /v1/refund-requests/upload-evidence | Upload Dispute Evidence File (Merchant) |

<a id="refundrequestslist"></a>
# **RefundRequestsList**
> void RefundRequestsList ()

List Refund Requests (Merchant)

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class RefundRequestsListExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            var apiInstance = new RefundRequestsApi(config);

            try
            {
                // List Refund Requests (Merchant)
                apiInstance.RefundRequestsList();
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RefundRequestsApi.RefundRequestsList: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RefundRequestsListWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Refund Requests (Merchant)
    apiInstance.RefundRequestsListWithHttpInfo();
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RefundRequestsApi.RefundRequestsListWithHttpInfo: " + e.Message);
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

<a id="refundrequestslistmessages"></a>
# **RefundRequestsListMessages**
> void RefundRequestsListMessages (string id)

List Messages for Refund Request (Merchant)

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class RefundRequestsListMessagesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            var apiInstance = new RefundRequestsApi(config);
            var id = "id_example";  // string | 

            try
            {
                // List Messages for Refund Request (Merchant)
                apiInstance.RefundRequestsListMessages(id);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RefundRequestsApi.RefundRequestsListMessages: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RefundRequestsListMessagesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Messages for Refund Request (Merchant)
    apiInstance.RefundRequestsListMessagesWithHttpInfo(id);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RefundRequestsApi.RefundRequestsListMessagesWithHttpInfo: " + e.Message);
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

<a id="refundrequestssendmessage"></a>
# **RefundRequestsSendMessage**
> void RefundRequestsSendMessage (string id)

Send Refund Request Message (Merchant)

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class RefundRequestsSendMessageExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            var apiInstance = new RefundRequestsApi(config);
            var id = "id_example";  // string | 

            try
            {
                // Send Refund Request Message (Merchant)
                apiInstance.RefundRequestsSendMessage(id);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RefundRequestsApi.RefundRequestsSendMessage: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RefundRequestsSendMessageWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Send Refund Request Message (Merchant)
    apiInstance.RefundRequestsSendMessageWithHttpInfo(id);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RefundRequestsApi.RefundRequestsSendMessageWithHttpInfo: " + e.Message);
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
| **201** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="refundrequestsupdatestatus"></a>
# **RefundRequestsUpdateStatus**
> void RefundRequestsUpdateStatus (string id)

Update Refund Request Status (Merchant)

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class RefundRequestsUpdateStatusExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            var apiInstance = new RefundRequestsApi(config);
            var id = "id_example";  // string | 

            try
            {
                // Update Refund Request Status (Merchant)
                apiInstance.RefundRequestsUpdateStatus(id);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RefundRequestsApi.RefundRequestsUpdateStatus: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RefundRequestsUpdateStatusWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Refund Request Status (Merchant)
    apiInstance.RefundRequestsUpdateStatusWithHttpInfo(id);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RefundRequestsApi.RefundRequestsUpdateStatusWithHttpInfo: " + e.Message);
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

<a id="refundrequestsuploadevidence"></a>
# **RefundRequestsUploadEvidence**
> void RefundRequestsUploadEvidence ()

Upload Dispute Evidence File (Merchant)

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Solifyn.Api;
using Solifyn.Client;
using Solifyn.Model;

namespace Example
{
    public class RefundRequestsUploadEvidenceExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8000";
            var apiInstance = new RefundRequestsApi(config);

            try
            {
                // Upload Dispute Evidence File (Merchant)
                apiInstance.RefundRequestsUploadEvidence();
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RefundRequestsApi.RefundRequestsUploadEvidence: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RefundRequestsUploadEvidenceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Upload Dispute Evidence File (Merchant)
    apiInstance.RefundRequestsUploadEvidenceWithHttpInfo();
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RefundRequestsApi.RefundRequestsUploadEvidenceWithHttpInfo: " + e.Message);
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

