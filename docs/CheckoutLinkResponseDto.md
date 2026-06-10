# Solifyn.Model.CheckoutLinkResponseDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **Guid** | The checkout link ID | 
**Title** | **string** | The title of the checkout link | [optional] 
**ProductId** | **string** | The linked Product ID | [optional] 
**CollectionId** | **string** | The linked Collection ID | [optional] 
**CustomerName** | **string** | Pre-filled customer name | [optional] 
**CustomerEmail** | **string** | Pre-filled customer email | [optional] 
**AddressLine1** | **string** | Pre-filled address line 1 | [optional] 
**City** | **string** | Pre-filled city | [optional] 
**State** | **string** | Pre-filled state | [optional] 
**PostalCode** | **string** | Pre-filled postal code | [optional] 
**Country** | **string** | Pre-filled country | [optional] 
**Quantity** | **decimal** | Quantity to purchase | 
**RedirectUrl** | **string** | URL to redirect to after successful payment | [optional] 
**CancelUrl** | **string** | URL to redirect to if payment is cancelled | [optional] 
**ShowDiscounts** | **bool** | Whether to show discounts on the checkout page | 
**CreatedAt** | **DateTime** | Timestamp when the link was created | 
**UpdatedAt** | **DateTime** | Timestamp when the link was last updated | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

