# Solifyn.Model.CreateCheckoutLinkDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Title** | **string** | The friendly display title of this checkout link | [optional] 
**ProductId** | **string** | Product database/Whop ID to sell | 
**CollectionId** | **string** | Optional collection database ID to sell | [optional] 
**CustomerName** | **string** | Prefilled customer name for checkout inputs | [optional] 
**CustomerEmail** | **string** | Prefilled customer email for checkout inputs | [optional] 
**AddressLine1** | **string** | Prefilled customer billing address line 1 | [optional] 
**City** | **string** | Prefilled customer billing city | [optional] 
**State** | **string** | Prefilled customer billing state | [optional] 
**PostalCode** | **string** | Prefilled customer billing zip/postal code | [optional] 
**Country** | **string** | Prefilled customer billing country (2-letter ISO) | [optional] 
**Quantity** | **Object** | Override quantity for checkout session | [optional] 
**RedirectUrl** | **string** | The absolute URL to redirect to upon successful payment completion | [optional] 
**CancelUrl** | **string** | The absolute URL to redirect to if a customer cancels the payment | [optional] 
**ShowDiscounts** | **bool** | Whether to display discount input form fields on checkout screen | [optional] [default to true]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

