# Solifyn.Model.OperationalWebhookEndpointInDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Url** | **string** | The URL to send webhook events to. | 
**Description** | **string** | Optional description for the endpoint. | [optional] 
**Disabled** | **bool** | Whether the endpoint is disabled. | [optional] [default to false]
**FilterTypes** | **List&lt;string&gt;** | The operational event types this endpoint will receive. | [optional] 
**Metadata** | **Object** | Metadata key-value pairs associated with the endpoint. | [optional] 
**Secret** | **string** | Optional custom endpoint signing secret (base64 encoded random bytes optionally prefixed with whsec_). If not set, the server will generate one. | [optional] 
**ThrottleRate** | **decimal** | Maximum messages per second to send to this endpoint (outgoing messages will be throttled to this rate). | [optional] 
**Uid** | **string** | Optional unique user-defined identifier for the endpoint. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

