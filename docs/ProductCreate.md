# Solifyn.Model.ProductCreate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** | Product display name. | 
**Description** | **string** | A description of the product. | [optional] 
**Price** | **decimal** | Price value. | 
**Currency** | **string** | Product pricing currency. | [default to CurrencyEnum.USD]
**ImageUrl** | **string** | URL of the product cover image. | [optional] 
**TaxCategory** | **string** | Tax classification. | 
**Discount** | **decimal** | Percentage or flat rate discount. | [optional] 
**HasLicenseKey** | **bool** | Whether to automatically issue license keys upon successful orders. | [optional] [default to false]
**HasDigitalDelivery** | **bool** | Whether the purchase includes downloadable files. | [optional] [default to false]
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

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

