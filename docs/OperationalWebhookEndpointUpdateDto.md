# Solifyn.Model.OperationalWebhookEndpointUpdateDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Url** | **string** | The URL to send webhook events to. | 
**Description** | **string** | Optional description for the endpoint. | [optional] 
**Disabled** | **bool** | Whether the endpoint is disabled. | [optional] 
**FilterTypes** | **List&lt;string&gt;** | The operational event types this endpoint will receive. | [optional] 
**Metadata** | **Object** | Metadata key-value pairs associated with the endpoint. | [optional] 
**ThrottleRate** | **decimal** | Maximum messages per second to send to this endpoint. | [optional] 
**Uid** | **string** | Optional unique user-defined identifier for the endpoint. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

