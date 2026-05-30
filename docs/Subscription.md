# Solifyn.Model.Subscription
Represents a customer subscription membership resource, containing current billing terms, plan, status, and metadata.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | The unique ID of the subscription | 
**Status** | **string** | The status of the subscription (e.g. completed, active, trialing, past_due, canceled) | 
**CreatedAt** | **DateTime** | Timestamp when the subscription was created | 
**JoinedAt** | **DateTime** | Timestamp when the member joined | 
**UpdatedAt** | **DateTime** | Timestamp when the subscription was last updated | 
**ManageUrl** | **string** | The management URL for the billing/subscription | 
**Member** | [**SubscriptionMemberDto**](SubscriptionMemberDto.md) | The member details | 
**User** | [**SubscriptionUserDto**](SubscriptionUserDto.md) | The user details | 
**RenewalPeriodStart** | **Object** | Start timestamp of the current renewal period | 
**RenewalPeriodEnd** | **Object** | End timestamp of the current renewal period | 
**CancelAtPeriodEnd** | **bool** | Whether the subscription is set to cancel at the end of the billing period | 
**CancelOption** | **Object** | The cancel option details | 
**CancellationReason** | **Object** | The reason for cancellation | 
**CanceledAt** | **Object** | Timestamp when the subscription was canceled | 
**Currency** | **string** | The currency used for payments | 
**Company** | [**SubscriptionCompanyDto**](SubscriptionCompanyDto.md) | The company context details | 
**Plan** | [**SubscriptionPlanDto**](SubscriptionPlanDto.md) | The plan associated with this subscription | 
**PromoCode** | **Object** | The promo code applied to the subscription | 
**Product** | [**SubscriptionProductDto**](SubscriptionProductDto.md) | The product associated with the subscription | 
**LicenseKey** | **Object** | The license key associated with this subscription | 
**Metadata** | **Object** | Additional metadata for the subscription | 
**PaymentCollectionPaused** | **bool** | Whether the payment collection is currently paused | 
**CheckoutConfigurationId** | **string** | The checkout configuration ID used | 
**Price** | **Object** | The price/amount of the membership | [optional] 
**Type** | **Object** | The type of the membership plan | [optional] 
**CustomerId** | **Object** | The business customer ID | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

