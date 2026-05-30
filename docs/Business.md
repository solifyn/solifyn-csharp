# Solifyn.Model.Business

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | The unique business ID | 
**Title** | **string** | Title or name of the business | 
**Description** | **string** | A description explaining what the business does | [optional] 
**WhopId** | **string** | The Whop Company ID | 
**MerchantId** | **string** | The merchant owner ID | 
**Verified** | **bool** | Whether the business has been KYC-verified on Whop | 
**SendCustomerEmails** | **bool** | Whether auto-emails are enabled for customers | 
**MemberCount** | **decimal** | Total members/customers under this business | 
**Route** | **string** | Whop friendly URL path route | [optional] 
**DefaultCurrency** | **string** | The default currency of the business | 
**PublishedReviewsCount** | **decimal** | Number of published user reviews on Whop | 
**Metadata** | **Object** | Custom key-value metadata | [optional] 
**TargetAudience** | **string** | The target audience description | [optional] 
**SocialLinks** | **Object** | Social links setup | [optional] 
**AffiliateInstructions** | **string** | Markdown instructions for affiliates | [optional] 
**WhopCreatedAt** | **DateTime** | Whop account creation timestamp | [optional] 
**WhopUpdatedAt** | **DateTime** | Whop account last updated timestamp | [optional] 
**CreatedAt** | **DateTime** | Timestamp when the business record was created | 
**UpdatedAt** | **DateTime** | Timestamp when the business record was last updated | 
**LogoUrl** | **string** | Brand logo image URL resolved from primary brand | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

