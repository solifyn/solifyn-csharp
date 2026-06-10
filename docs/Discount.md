# Solifyn.Model.Discount
Represents a discount code created under your business, containing type, amount, usage limits, and expiration details.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | The unique prefix-based identifier of the discount (e.g., &#x60;disc_cs8f67sd7f6fw3fs&#x60;). | 
**DiscountId** | **string** | Alias for the unique identifier of the discount. | 
**Code** | **string** | The unique discount code (e.g. SAVE10) used during checkout. | 
**Name** | **string** | The customer-facing name of the discount code (e.g. Summer Sale). | [optional] 
**Type** | **string** | The discount calculation type: percentage or fixed_amount. | 
**Amount** | **int** | The discount value. For percentage type, it is in basis points (e.g. 1000 &#x3D; 10.00%). For fixed_amount type, it is in cents (e.g. 1000 &#x3D; $10.00). | 
**UsageLimit** | **int** | Maximum number of times this discount code can be redeemed. Null represents unlimited usage. | 
**TimesUsed** | **int** | The number of times this discount code has been successfully redeemed. | 
**ExpiresAt** | **DateTime** | The expiration timestamp after which the discount code is no longer valid. | 
**Status** | **string** | The current status of the discount. | 
**BusinessId** | **string** | The unique identifier associated with the business this discount belongs to. | 
**CreatedAt** | **DateTime** | Timestamp indicating exactly when the discount was created. | 
**UpdatedAt** | **DateTime** | Timestamp indicating when the discount was last updated. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

