# Solifyn.Model.SubscriptionSeatAdjustment
Represents the detailed cost and billing impact of adjusting subscription seat add-on quantities.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Success** | **bool** | Indicates if the seat adjustment was successful | 
**SubscriptionId** | **string** | The customer subscription ID | 
**AddonProductId** | **string** | The unique ID of the addon product | 
**OldQuantity** | **decimal** | The previous seat quantity | 
**NewQuantity** | **decimal** | The new seat quantity after adjustment | 
**QuantityDelta** | **decimal** | The difference in seat quantity | 
**ProrationType** | **string** | The proration strategy type applied | 
**CostImpact** | **decimal** | Calculated pro-rata price cost impact in currency unit (charged or credited) | 
**Currency** | **string** | Billing currency | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

