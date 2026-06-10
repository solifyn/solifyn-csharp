# Solifyn.Model.LicensesCreateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProductId** | **Guid** | The unique product identifier (internal product ID or ID) for which the license key will be issued. | 
**CustomerId** | **string** | The unique customer identifier (internal customer ID or ID) who will own this license key. | 
**ActivationLimit** | **int** | The maximum number of concurrent device or server activations allowed for this license key. | [optional] 
**ExpiryHours** | **int** | Relative validity period of the license in hours starting from the time of creation. | [optional] 
**Key** | **string** | Optional custom license key string. If not provided, a random uppercase cryptographic serial key (e.g., ABCD-EFGH) will be generated automatically. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

