# Solifyn.Model.DiscountCreate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Code** | **string** | Unique discount code string (will be automatically capitalized). | 
**Name** | **string** | Customer-facing name of the discount. | [optional] 
**Type** | **string** | Calculation type: percentage or fixed_amount. | 
**Amount** | **decimal** | The discount value. If percentage, enter value like 10 for 10%. If fixed_amount, enter value like 10 for $10.00. | 
**UsageLimit** | **int** | Maximum number of redemptions allowed. | [optional] 
**ExpiresAt** | **DateTime** | Expiration timestamp for the discount. | [optional] 
**SubscriptionCycles** | **int** | Number of subscription cycles this discount applies to. | [optional] 
**RestrictedTo** | **List&lt;string&gt;** | List of product IDs this discount is restricted to. | [optional] 
**PreserveOnPlanChange** | **bool** | Whether to preserve the discount when subscription plan changes. | [optional] 
**Metadata** | **Object** | Custom metadata for the discount. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

