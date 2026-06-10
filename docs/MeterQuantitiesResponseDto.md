# Solifyn.Model.MeterQuantitiesResponseDto
Represents aggregated usage quantities and calculated product costs for a meter within a selected date range.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**MeterId** | **string** | The unique meter ID. | 
**Name** | **string** | Meter display name. | 
**TotalUsage** | **decimal** | Total usage within the selected time range. | 
**Costs** | [**List&lt;MeterQuantitiesCostDto&gt;**](MeterQuantitiesCostDto.md) | Cost breakdown for products attached to the meter. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

