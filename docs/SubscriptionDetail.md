# Solifyn.Model.SubscriptionDetail
Represents detailed information about a customer subscription including active base product configuration, billing and payment history, and purchased add-ons.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Subscription** | [**Subscription**](Subscription.md) | The main subscription details | 
**Payments** | [**List&lt;Order&gt;**](Order.md) | The subscription payments / invoice billing history | 
**PurchasedAddons** | [**List&lt;ResolvedAddon&gt;**](ResolvedAddon.md) | List of purchased addons associated with this subscription | 
**Product** | [**SubscriptionDetailProduct**](SubscriptionDetailProduct.md) | The core product information associated with this subscription | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

