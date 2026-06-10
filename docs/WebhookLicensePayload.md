# Solifyn.Model.WebhookLicensePayload
Represents a cryptographically secure software license key issued to a customer upon purchase or manual issuance.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | The unique prefix-based identifier of the license key. | 
**Key** | **string** | The cryptographically generated license key string delivered to the customer. | 
**Status** | **string** | Lifecycle status of the license. ACTIVE &#x3D; active. DISABLED &#x3D; suspended. REVOKED &#x3D; hard-revoked. | 
**BusinessId** | **string** | The unique identifier associated with the business this license belongs to. | 
**ProductId** | **string** | The unique ID of the product this license key is associated with. | 
**PaymentId** | **string** | The unique payment identifier that triggered the issuance of this license key. | 
**CustomerId** | **string** | The unique customer identifier (ID) who received this license key. | 
**ActivationLimit** | **decimal?** | Maximum number of simultaneous active device instances allowed for this license. Null means unlimited. | 
**ActivationMessage** | **string** | Optional message displayed to the customer upon successful activation. | 
**InstancesCount** | **decimal** | Running count of how many times this license key has been activated. | 
**ExpiryHours** | **decimal?** | Relative expiry duration in hours from the time of issuance. | 
**ExpiresAt** | **string** | Absolute expiration timestamp. The license becomes invalid after this point. | 
**Filters** | **Object** | Optional custom metadata filters associated with the license. | 
**Archived** | **bool** | Indicates if the license key is archived. | 
**CreatedAt** | **string** | Timestamp indicating exactly when the license key was issued. | 
**UpdatedAt** | **string** | Timestamp indicating when the license key was last modified. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

