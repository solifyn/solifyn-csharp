# Solifyn.Model.Dispute

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | The dispute ID | 
**WhopId** | **string** | The Whop Dispute ID | 
**Amount** | **decimal** | The dispute amount | 
**Currency** | **string** | The currency code | 
**Status** | **string** | The status of the dispute | 
**Reason** | **string** | The reason for the dispute | [optional] 
**Editable** | **bool** | Whether the evidence is still editable | 
**NeedsResponseBy** | **DateTime** | Timestamp by when evidence must be submitted | [optional] 
**VisaRdr** | **bool** | Whether Visa RDR was applied | 
**BillingAddress** | **string** | Customer billing address details | [optional] 
**CustomerName** | **string** | Customer name | [optional] 
**CustomerEmail** | **string** | Customer email address | [optional] 
**Notes** | **string** | Additional notes | [optional] 
**ProductDescription** | **string** | Product or service description | [optional] 
**ServiceDate** | **string** | Service or purchase date | [optional] 
**AccessActivityLog** | **string** | Log of access activity | [optional] 
**Evidence** | [**DisputeEvidenceDto**](DisputeEvidenceDto.md) | Evidence attachments associated with the dispute | [optional] 
**PaymentId** | **string** | The associated payment ID | 
**BusinessId** | **string** | The associated business ID | 
**CreatedAt** | **DateTime** | Timestamp when the dispute was created | 
**UpdatedAt** | **DateTime** | Timestamp when the dispute was last updated | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

