# Solifyn.Model.SubscriptionAction

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**FreeDays** | **decimal** | Number of free days to add (used with action: add_free_days) | [optional] 
**CancellationMode** | **string** | Cancellation mode (used with action: cancel) | [optional] 
**VoidPayments** | **bool** | Whether to void subsequent payments (used with action: pause) | [optional] 
**AddonProductId** | **string** | ID of the addon product to adjust seats for (used with action: adjust_seats) | [optional] 
**NewQuantity** | **decimal** | The new seat quantity (used with action: adjust_seats) | [optional] 
**ProrationType** | **string** | Proration strategy mode (used with action: adjust_seats) | [optional] 
**IdempotencyKey** | **string** | A unique idempotency key to prevent duplicate mutative actions for network transient retries. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

