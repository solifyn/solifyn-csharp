# Solifyn.Model.OrderRefundCreate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Amount** | **int** | The refund amount in cents. If full refund is true, this can represent the total amount. | 
**IsFullRefund** | **bool** | Whether this is a full refund or a partial refund. | 
**IdempotencyKey** | **string** | A unique idempotency key to prevent double refunds for transient network retries. | 
**AutoRevokeSeats** | **bool** | Whether to automatically revoke seat add-ons matching the refund amount. | [optional] 
**RevokeSeats** | [**List&lt;RevokeSeatDto&gt;**](RevokeSeatDto.md) | List of specific addons and the quantities of seats to revoke. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

