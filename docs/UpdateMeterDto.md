# Solifyn.Model.UpdateMeterDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** | Meter display name. | [optional] 
**Description** | **string** | Meter description. | [optional] 
**EventName** | **string** | The event name tracked by this meter. | [optional] 
**AggregationType** | **string** | Aggregation strategy for usage events. | [optional] 
**AggregationKey** | **string** | Metadata key used by SUM, MAX, or LAST aggregation modes. | [optional] 
**Unit** | **string** | Measurement unit label. | [optional] 
**Filters** | **Dictionary&lt;string, Object&gt;** | Optional filter definition for advanced matching. | [optional] 
**EnableFiltering** | **bool** | Enable filtering on usage event ingestion. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

