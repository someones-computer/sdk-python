# ManagedServiceQuotaBytes

Byte ceiling this service must not exceed; null where none is set.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------

## Example

```python
from someones_computer_sdk.models.managed_service_quota_bytes import ManagedServiceQuotaBytes

# TODO update the JSON string below
json = "{}"
# create an instance of ManagedServiceQuotaBytes from a JSON string
managed_service_quota_bytes_instance = ManagedServiceQuotaBytes.from_json(json)
# print the JSON string representation of the object
print(ManagedServiceQuotaBytes.to_json())

# convert the object into a dict
managed_service_quota_bytes_dict = managed_service_quota_bytes_instance.to_dict()
# create an instance of ManagedServiceQuotaBytes from a dict
managed_service_quota_bytes_from_dict = ManagedServiceQuotaBytes.from_dict(managed_service_quota_bytes_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


