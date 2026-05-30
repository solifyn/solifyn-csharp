# Solifyn.Model.CollectionProductDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **Guid** | The unique identifier (ID) of the product. | 
**Name** | **string** | The display name of the product. | 
**Price** | **decimal** | The price amount of the product (e.g. 29.00). | 
**Currency** | **string** | The three-letter ISO currency code (e.g. USD, VND, EUR). | 
**Description** | **string** | A comprehensive rich text description of the product. | [optional] 
**Status** | **string** | The lifecycle status of the product (e.g. ACTIVE, ARCHIVED). | 
**ImageUrl** | **string** | URL of the product cover image. | 
**TaxCategory** | **string** | The tax classification for the product. | 
**PricingType** | **string** | Pricing model of the product. | 
**Discount** | **decimal** | Discount value as a percentage or fixed amount. | 
**HasLicenseKey** | **bool** | Indicates if the product issues a cryptographically secure software license key upon checkout completion. | 
**HasDigitalDelivery** | **bool** | Whether the product includes digital file downloads upon purchase. | 
**IsTaxInclusive** | **bool** | Whether the product price already includes applicable sales taxes. | 
**BillingPeriod** | **int** | The subscription billing cycle interval in days (for subscription products). | 
**TrialPeriodDays** | **int** | Trial duration in days for subscription products. | 
**ExpirationDays** | **int** | Automatic expiration period in days for the subscription entitlement. | 
**StatementDescriptor** | **string** | Custom text displayed on customer credit card statements for purchases of this product. | 
**PayWhatYouWant** | **bool** | Indicates if customers are allowed to enter a custom pricing amount at checkout. | 
**Metadata** | **Dictionary&lt;string, string&gt;** | Custom developer metadata key-value pairs associated with the product. | 
**CustomFields** | **List&lt;Object&gt;** | Custom form field questions to ask the customer during checkout. | 
**Stock** | **int** | Available stock quantity, or null for unlimited inventory. | 
**ActivationLimit** | **int** | Maximum number of simultaneous active instances/devices allowed per issued license key (applicable if hasLicenseKey is true). | 
**IsListed** | **bool** | Defines if the product is listed publicly on the merchant&#39;s storefront template. | 
**CreatedAt** | **DateTime** | Timestamp indicating exactly when the product was created. | 
**UpdatedAt** | **DateTime** | Timestamp indicating when the product was last modified. | 
**IsPermanentlyDeleted** | **bool** | Indicates if the product has been permanently deleted. | 
**BrandId** | **string** | Optional brand identifier. | 
**DigitalLink** | **string** | Secure link for digital delivery. | 
**Instructions** | **string** | Special instructions provided upon purchase. | 
**ActivationMessage** | **string** | Custom message displayed when a license key is activated. | 
**ExpiryHours** | **int** | Number of hours until the license key expires. | 
**BusinessId** | **string** | The unique identifier of the business owning this product. | 
**Quantity** | **decimal** | Quantity of the product in the collection | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

