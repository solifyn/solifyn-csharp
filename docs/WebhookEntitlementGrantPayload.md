# Solifyn.Model.WebhookEntitlementGrantPayload

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **Guid** | The unique entitlement grant ID. | [optional] 
**BusinessId** | **Guid** | The business ID context. | [optional] 
**CustomerId** | **Guid** | The customer ID. | [optional] 
**PaymentId** | **Guid?** | Associated payment transaction ID. | [optional] 
**ProductId** | **Guid** | The purchased product ID. | [optional] 
**Type** | **string** | The type of entitlement (e.g. GITHUB). | [optional] 
**GithubRepo** | **string** | Target GitHub repository (owner/repo) if type is GITHUB. | [optional] 
**GithubPermission** | **string** | GitHub access permission level if type is GITHUB. | [optional] 
**GithubUsername** | **string** | The connected customer GitHub username. | [optional] 
**Status** | **string** | Delivery status of the collaborator invite (PENDING, DELIVERED, FAILED, REVOKED). | [optional] 
**OauthUrl** | **string** | OAuth URL to redirect the customer to. | [optional] 
**ErrorDetails** | **string** | Error message if invitation delivery failed. | [optional] 
**CreatedAt** | **DateTime** |  | [optional] 
**UpdatedAt** | **DateTime** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

