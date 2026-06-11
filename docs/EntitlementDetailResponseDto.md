# Solifyn.Model.EntitlementDetailResponseDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | The unique entitlement ID | 
**BusinessId** | **string** | The owning business ID | 
**Name** | **string** | The name of the entitlement | 
**Type** | **string** | The type of access to grant | 
**Status** | **string** | Status of the entitlement | 
**CreatedAt** | **DateTime** | When the entitlement was created | 
**UpdatedAt** | **DateTime** | When the entitlement was last updated | 
**GithubRepo** | **string** | The GitHub repository (e.g., owner/repo) | [optional] 
**GithubPermission** | **string** | The GitHub repository permission level | [optional] 
**DiscordGuildId** | **string** | The Discord Guild/Server ID | [optional] 
**DiscordRoleId** | **string** | The Discord Role ID to assign | [optional] 
**FramerTemplateId** | **string** | The associated Framer Template ID | [optional] 
**LicenseKey** | **string** | The static License Key (if not dynamically generated) | [optional] 
**ActivationLimit** | **decimal** | The maximum activation limit for licenses | [optional] 
**ActivationMessage** | **string** | A message shown to the user upon license activation | [optional] 
**ExpiryHours** | **decimal** | The number of hours until the entitlement expires | [optional] 
**DigitalLink** | **string** | The digital download URL or redirect link | [optional] 
**Instructions** | **string** | Custom setup instructions for the user | [optional] 
**GrantsCount** | **decimal** | Number of active customer grants issued from this entitlement | 
**Products** | [**List&lt;LinkedProductDto&gt;**](LinkedProductDto.md) | Products that are currently linked to this entitlement | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

