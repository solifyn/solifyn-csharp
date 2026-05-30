# Solifyn.Model.CreateCheckoutDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProductId** | **string** | The public product identifier (product ID) | 
**Currency** | **string** | Three-letter ISO currency code (lowercase) | [optional] 
**Quantity** | **decimal** | The quantity of items to buy | [optional] [default to 1M]
**DiscountCode** | **string** | Discount code to apply | [optional] 
**CustomPrice** | **decimal** | Custom price paid by customer (for Pay What You Want products) | [optional] 
**CustomerEmail** | **string** | Email address of the customer | [optional] 
**CheckoutData** | **Object** | JSON metadata or checkout custom information | [optional] 
**CustomFields** | **Object** | Custom text fields required for the purchase | [optional] 
**Aff** | **string** | Affiliate partner tracking code | [optional] 
**CheckoutId** | **string** | The existing checkout database ID to validate / update | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

