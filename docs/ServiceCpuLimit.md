# ServiceCpuLimit

Nanoseconds of CPU (compose deploy.resources.limits.cpus), null = unset.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------

## Example

```python
from someones_computer_sdk.models.service_cpu_limit import ServiceCpuLimit

# TODO update the JSON string below
json = "{}"
# create an instance of ServiceCpuLimit from a JSON string
service_cpu_limit_instance = ServiceCpuLimit.from_json(json)
# print the JSON string representation of the object
print(ServiceCpuLimit.to_json())

# convert the object into a dict
service_cpu_limit_dict = service_cpu_limit_instance.to_dict()
# create an instance of ServiceCpuLimit from a dict
service_cpu_limit_from_dict = ServiceCpuLimit.from_dict(service_cpu_limit_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


