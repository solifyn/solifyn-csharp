# Solifyn.Model.AddonCreate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProductId** | **string** | The product ID of the addon product. | 
**MinQuantity** | **decimal** | Minimum quantity of the addon allowed to be purchased. | [default to 0M]
**MaxQuantity** | **decimal** | Maximum quantity of the addon allowed to be purchased (optional). | [optional] 
**PriceOverride** | **decimal** | Price override for the addon product when purchased with this parent (optional). | [optional] 
**IsSeatAddon** | **bool** | Flag indicating if this addon represents a seat/license limit increment. | [default to false]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

