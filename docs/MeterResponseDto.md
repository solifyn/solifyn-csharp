# Solifyn.Model.MeterResponseDto
Represents a usage meter configured for event-based billing, including the tracked event name, aggregation strategy, optional filters, and archive status.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | The unique meter ID. | 
**BusinessId** | **string** | The business ID that owns this meter. | 
**Name** | **string** | Meter display name. | 
**Description** | **Object** | Meter description. | [optional] 
**EventName** | **string** | The event name tracked by this meter. | 
**AggregationType** | **string** | Aggregation strategy for usage events. | 
**AggregationKey** | **Object** | Metadata key used for aggregation. | [optional] 
**Unit** | **Object** | Measurement unit label. | [optional] 
**Filters** | **Dictionary&lt;string, Object&gt;** | Optional filter definition for advanced matching. | [optional] 
**Archived** | **bool** | Whether the meter is archived. | 
**CreatedAt** | **DateTime** | Creation timestamp. | 
**UpdatedAt** | **DateTime** | Last update timestamp. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

