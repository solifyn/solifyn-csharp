# Solifyn.Model.Withdrawal

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | The local withdrawal ID | 
**WhopId** | **string** | The Whop withdrawal ID | 
**Amount** | **decimal** | The amount withdrawn in cents | 
**Currency** | **string** | Three-letter ISO currency code | 
**Status** | **string** | The status of the withdrawal request | 
**FeeAmount** | **decimal** | Fee amount charged for the withdrawal in cents | [optional] 
**FeeType** | **string** | The fee structure type (inclusive or exclusive) | [optional] 
**MarkupFee** | **decimal** | Markup fee applied in cents | [optional] 
**Speed** | **string** | Speed of withdrawal (standard, instant) | [optional] 
**TraceCode** | **string** | Bank trace or reference code for tracking the payout | [optional] 
**PayerName** | **string** | The name of the entity or account paying out | [optional] 
**ErrorMessage** | **string** | Error message if the withdrawal failed | [optional] 
**BusinessId** | **string** | The business ID associated with this withdrawal | 
**CreatedAt** | **DateTime** | Timestamp when the withdrawal was requested | 
**UpdatedAt** | **DateTime** | Timestamp when the withdrawal status was updated | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

