# Solifyn.Model.Refund

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **Guid** | The refund ID | 
**WhopId** | **string** | The Whop Refund ID | 
**IdempotencyKey** | **string** | Client-generated key to prevent duplicate refunds | [optional] 
**Amount** | **decimal** | Refunded amount | 
**Currency** | **string** | Currency code | 
**Status** | **string** | Status of the refund | 
**Provider** | **string** | The payment provider used | [optional] 
**Reason** | **string** | Reason for the refund | [optional] 
**ReferenceValue** | **string** | Acquirer Reference Number (ARN) or tracking number | [optional] 
**PaymentId** | **Guid** | The associated Payment ID | 
**ProviderCreatedAt** | **DateTime?** | Timestamp when the refund was processed by the provider | [optional] 
**CreatedAt** | **DateTime** | Timestamp when the refund was created in our system | 
**UpdatedAt** | **DateTime** | Timestamp when the refund was last updated | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

