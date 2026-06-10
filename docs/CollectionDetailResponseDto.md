# Solifyn.Model.CollectionDetailResponseDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **Guid** | The collection ID | 
**Name** | **string** | The name of the collection | 
**Description** | **string** | A brief description of the collection | [optional] 
**ImageUrl** | **string** | URL of the collection image | [optional] 
**Status** | **string** | Status of the collection | 
**BusinessId** | **string** | The unique identifier of the business owning this collection. | 
**IsPermanentlyDeleted** | **bool** | Indicates if the collection has been permanently deleted. | 
**CreatedAt** | **DateTime** | Timestamp when the collection was created | 
**UpdatedAt** | **DateTime** | Timestamp when the collection was last updated | 
**Products** | [**List&lt;CollectionProductDto&gt;**](CollectionProductDto.md) | Full product details including quantity for each item in the collection | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

