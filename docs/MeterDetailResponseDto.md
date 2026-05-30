# Solifyn.Model.MeterDetailResponseDto
Represents a usage meter with its most recent usage events and total usage event count.

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
**UsageEvents** | [**List&lt;MeterUsageEventDto&gt;**](MeterUsageEventDto.md) | Most recent usage events recorded for the meter. | 
**TotalUsageEvents** | **decimal** | Total usage event count for the meter. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

