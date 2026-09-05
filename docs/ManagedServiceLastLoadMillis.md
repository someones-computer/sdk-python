# ManagedServiceLastLoadMillis

The engine's own cumulative exec-time counter as of the last sample, in milliseconds — the baseline {@see \\App\\Service\\ManagedService\\LoadSampler} subtracts from the next reading to get a delta, the same shape {@see \\App\\Entity\\Task::$lastCpuNanos} uses for a container's CPU rate.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------

## Example

```python
from someones_computer_sdk.models.managed_service_last_load_millis import ManagedServiceLastLoadMillis

# TODO update the JSON string below
json = "{}"
# create an instance of ManagedServiceLastLoadMillis from a JSON string
managed_service_last_load_millis_instance = ManagedServiceLastLoadMillis.from_json(json)
# print the JSON string representation of the object
print(ManagedServiceLastLoadMillis.to_json())

# convert the object into a dict
managed_service_last_load_millis_dict = managed_service_last_load_millis_instance.to_dict()
# create an instance of ManagedServiceLastLoadMillis from a dict
managed_service_last_load_millis_from_dict = ManagedServiceLastLoadMillis.from_dict(managed_service_last_load_millis_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


