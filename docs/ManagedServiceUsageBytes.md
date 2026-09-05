# ManagedServiceUsageBytes

Latest metered size. Suspended services keep reporting it — they are still billed for storage.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------

## Example

```python
from someones_computer_sdk.models.managed_service_usage_bytes import ManagedServiceUsageBytes

# TODO update the JSON string below
json = "{}"
# create an instance of ManagedServiceUsageBytes from a JSON string
managed_service_usage_bytes_instance = ManagedServiceUsageBytes.from_json(json)
# print the JSON string representation of the object
print(ManagedServiceUsageBytes.to_json())

# convert the object into a dict
managed_service_usage_bytes_dict = managed_service_usage_bytes_instance.to_dict()
# create an instance of ManagedServiceUsageBytes from a dict
managed_service_usage_bytes_from_dict = ManagedServiceUsageBytes.from_dict(managed_service_usage_bytes_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


