# Solifyn.Model.Instance
Represents an active device or software instance that has been activated against a license key.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | The unique database identifier of this instance record. | 
**LicenseId** | **string** | The internal ID of the parent license key this instance belongs to. | 
**InstanceId** | **string** | The unique hardware hash or client-generated identifier of the activated device/machine. | 
**InstanceName** | **string** | A human-readable display name for this instance, assigned by the client application. | 
**IpAddress** | **string** | The IP address recorded at the time of activation. | 
**ActivatedAt** | **string** | Timestamp when this device instance was first activated. | 
**LastSeenAt** | **string** | Timestamp of the most recent activation heartbeat or re-activation check from this device. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

