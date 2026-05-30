# Solifyn.Model.CheckoutSessionDetailsDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Checkout session identifier | 
**Price** | **decimal** | Total purchase amount | 
**Currency** | **string** | ISO currency code of the purchase | 
**StoreName** | **string** | Title or name of the merchant/store selling the item | 
**Status** | **string** | Current status of the checkout session | 
**BillingAddress** | **Object** | Customer billing address details | [optional] 
**CustomFields** | **Object** | Custom fields collected during purchase | [optional] 
**SessionId** | **string** | The payment partner session ID | [optional] 
**PaymentId** | **string** | Database payment transaction ID | [optional] 
**CheckoutUrl** | **string** | Checkout session redirect URL if loaded in link mode | [optional] 
**Product** | [**Product**](Product.md) | The details of the product being purchased | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

