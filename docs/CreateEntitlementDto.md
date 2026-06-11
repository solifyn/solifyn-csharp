# Solifyn.Model.CreateEntitlementDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** | The user-friendly name of the entitlement | 
**Type** | **string** | The type of access to grant | 
**GithubRepo** | **string** | The GitHub repository (e.g., owner/repo) | [optional] 
**GithubPermission** | **string** | The GitHub repository permission level | [optional] [default to "pull"]
**DiscordGuildId** | **string** | The Discord Guild/Server ID | [optional] 
**DiscordRoleId** | **string** | The Discord Role ID to assign | [optional] 
**FramerTemplateId** | **string** | The associated Framer Template ID | [optional] 
**LicenseKey** | **string** | The static License Key (if not dynamically generated) | [optional] 
**ActivationLimit** | **decimal** | The maximum activation limit for licenses | [optional] 
**ActivationMessage** | **string** | A message shown to the user upon license activation | [optional] 
**ExpiryHours** | **decimal** | The number of hours until the entitlement expires | [optional] 
**DigitalLink** | **string** | The digital download URL or redirect link | [optional] 
**Instructions** | **string** | Custom setup instructions for the user | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

