# Solifyn.Model.Order
Represents an order (payment) processed under your business, containing customer, billing, product cart, and refund details.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Unique internal database identifier. | 
**InvoiceUrl** | **string** | The invoice print URL. | 
**Customer** | [**OrderCustomer**](OrderCustomer.md) | Customer details. | 
**TotalAmount** | **int** | Total paid amount in cents. | 
**Subtotal** | **int** | Subtotal amount in cents. | 
**TaxAmount** | **int** | Tax amount in cents. | 
**ApplicationFee** | **int** | Application fee in cents. | 
**AmountAfterFees** | **int** | Net amount after fees in cents. | 
**Currency** | **string** | Currency code. | 
**Status** | **string** | Current status of the payment. | 
**CreatedAt** | **DateTime** | Payment creation timestamp. | 
**PaidAt** | **DateTime** | Payment completion/paid timestamp. | [optional] 
**PaymentMethod** | **string** | Payment method utilized. | 
**CardLastFour** | **string** | Last four digits of card used. | [optional] 
**CardNetwork** | **string** | Card network/brand. | [optional] 
**CardType** | **string** | Card type. | [optional] 
**Billing** | [**OrderBilling**](OrderBilling.md) | Billing address details. | [optional] 
**ProductCart** | [**List&lt;OrderProductCart&gt;**](OrderProductCart.md) | Products purchased in this order. | 
**Metadata** | **Object** | Custom metadata payload associated with this payment. | [optional] 
**VarOrder** | [**OrderDetail**](OrderDetail.md) | Order details snapshot. | [optional] 
**Refundable** | **bool** | Indicates whether the order is eligible for refund. | 
**Refunds** | [**List&lt;OrderRefund&gt;**](OrderRefund.md) | List of refunds associated with this payment. | [optional] 
**BusinessId** | **string** | Business unique ID identifier. | 
**BusinessName** | **string** | Business display title/name. | 
**BillingReason** | **string** | Billing reason detail. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

