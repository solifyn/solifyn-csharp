# Solifyn.Model.EntitlementGrantResponseDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **Guid** | The unique entitlement grant ID. | 
**BusinessId** | **Guid** | The business ID context. | 
**CustomerId** | **Guid** | The customer ID. | 
**PaymentId** | **Guid** | Associated payment transaction ID. | [optional] 
**ProductId** | **Guid** | The purchased product ID. | 
**Type** | **string** | The type of entitlement (e.g. GITHUB, DISCORD, TELEGRAM). | 
**GithubRepo** | **string** | Target GitHub repository (owner/repo) if type is GITHUB. | [optional] 
**GithubPermission** | **string** | GitHub access permission level if type is GITHUB. | [optional] 
**GithubUsername** | **string** | The connected customer GitHub username. | [optional] 
**DiscordGuildId** | **string** | Target Discord Guild ID if type is DISCORD. | [optional] 
**DiscordRoleId** | **string** | Target Discord Role ID if type is DISCORD. | [optional] 
**DiscordUsername** | **string** | The connected customer Discord username. | [optional] 
**DiscordUserId** | **string** | The connected customer Discord user ID. | [optional] 
**FramerTemplateId** | **Guid** | The Framer template ID if type is FRAMER. | [optional] 
**FramerRemixLink** | **string** | The single-use remix link generated for the customer if type is FRAMER. | [optional] 
**Status** | **string** | Delivery status of the collaborator invite (PENDING, DELIVERED, FAILED, REVOKED). | 
**OauthUrl** | **string** | OAuth URL to redirect the customer to. | [optional] 
**ErrorDetails** | **string** | Error message if invitation delivery failed. | [optional] 
**Metadata** | **Object** | Platform-specific metadata. | [optional] 
**CreatedAt** | **string** | Creation timestamp. | 
**UpdatedAt** | **string** | Modification timestamp. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

