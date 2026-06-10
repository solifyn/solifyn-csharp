# Solifyn.Model.MeterIngestEventDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**EventId** | **string** | Unique usage event ID for idempotency. | 
**CustomerId** | **string** | Unique customer ID associated with the event. | 
**EventName** | **string** | Event name that should match a meter eventName. | 
**Value** | **decimal** | Event quantity value. | [optional] [default to 1M]
**Metadata** | **Dictionary&lt;string, Object&gt;** | Metadata attached to the usage event. | [optional] 
**Timestamp** | **string** | Timestamp of the event in ISO 8601 format. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

