# Solifyn.Model.ProductUpdate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** | Product display name. | [optional] 
**Description** | **string** | A description of the product. | [optional] 
**Price** | **decimal** | Price value. | [optional] 
**Currency** | **string** | Product pricing currency. | [optional] [default to CurrencyEnum.USD]
**ImageUrl** | **string** | URL of the product cover image. | [optional] 
**TaxCategory** | **string** | Tax classification. | [optional] 
**Discount** | **decimal** | Percentage or flat rate discount. | [optional] 
**HasLicenseKey** | **bool** | Whether to automatically issue license keys upon successful orders. | [optional] [default to false]
**HasDigitalDelivery** | **bool** | Whether the purchase includes downloadable files. | [optional] [default to false]
**HasGithubAccess** | **bool** | Whether the purchase includes GitHub repository access. | [optional] [default to false]
**GithubRepo** | **string** | GitHub repository to grant access to (format: owner/repo). | [optional] 
**GithubPermission** | **string** | GitHub collaborator permission level. | [optional] 
**HasDiscordAccess** | **bool** | Whether the purchase includes Discord server role access. | [optional] [default to false]
**DiscordGuildId** | **string** | Discord Guild (Server) ID to grant access to. | [optional] 
**DiscordRoleId** | **string** | Discord Role ID to assign to the user. | [optional] 
**IsTaxInclusive** | **bool** | Whether tax is included in the base price. | [optional] [default to false]
**ActivationLimit** | **int** | Maximum concurrent activated instances allowed per license key. | [optional] 
**BrandId** | **string** | Brand id for the product, if not provided will default to primary brand. | [optional] 
**BillingPeriod** | **int** | Billing period in days (for Subscription products). | [optional] 
**TrialPeriodDays** | **int** | Trial duration in days. | [optional] 
**ExpirationDays** | **int** | Subscription expiration duration in days. | [optional] 
**StatementDescriptor** | **string** | Custom billing descriptor. | [optional] 
**PayWhatYouWant** | **bool** | Allow pay-what-you-want pricing. | [optional] [default to false]
**Metadata** | **Dictionary&lt;string, string&gt;** | Developer key-value metadata pairs. | [optional] 
**CustomFields** | [**List&lt;ProductCreateCustomFieldsInner&gt;**](ProductCreateCustomFieldsInner.md) | Form field configurations to gather during checkout. | [optional] 
**Stock** | **int** | Initial stock quantity limit. | [optional] 
**IsListed** | **bool** | Whether the product is publicly visible. | [optional] [default to true]
**IsFree** | **bool** | Whether the product is free of charge. | [optional] [default to false]
**Addons** | [**List&lt;ProductCreateAddonsInner&gt;**](ProductCreateAddonsInner.md) | Product addons configurations. | [optional] 
**EntitlementIds** | **List&lt;string&gt;** | Array of independent entitlement IDs to link to this product. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

