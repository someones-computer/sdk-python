# ServiceInstance


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Operator-facing handle, unique across the estate: &#x60;pg17-1&#x60;, &#x60;mysql80-1&#x60;. | [optional] 
**kind** | **str** |  | [optional] 
**major_version** | **str** | The major version this engine *is*, as the catalogue names it: &#x60;17&#x60;, &#x60;16&#x60;, &#x60;11.8&#x60;, &#x60;8.4&#x60;, &#x60;8.0&#x60;. | [optional] 
**image_ref** | **str** | The exact image this instance runs, pinned — never a floating upstream tag. | [optional] 
**swarm** | **str** | Repoint the instance at a different context. | [optional] 
**overlay_network** | **str** | The internal overlay this engine and every sidecar bound to it share. | [optional] 
**state** | **str** | Moving to any state other than {@see ServiceInstanceState::Failed} clears a stale failure. | [optional] [default to 'requested']
**failure_reason** | **str** | Why the instance failed, carried beside the state as &#x60;Machine::$failure&#x60; already does. | [optional] [readonly] 
**capacity_bytes** | [**ServiceInstanceCapacityBytes**](ServiceInstanceCapacityBytes.md) |  | [optional] 
**observed_usage_bytes** | [**ServiceInstanceObservedUsageBytes**](ServiceInstanceObservedUsageBytes.md) |  | [optional] 
**observed_at** | **datetime** |  | [optional] [readonly] 
**id** | **str** |  | [optional] [readonly] 
**created_at** | **datetime** |  | [optional] [readonly] 
**updated_at** | **datetime** |  | [optional] [readonly] 
**catalogue_entry** | **str** | &#x60;postgres 17&#x60;, &#x60;mysql 8.0&#x60; — the catalogue entry this instance serves. | [optional] [readonly] 
**serving** | **bool** |  | [optional] [readonly] 
**admin_credential** | [**SealedSecret**](SealedSecret.md) |  | [optional] 

## Example

```python
from someones_computer_sdk.models.service_instance import ServiceInstance

# TODO update the JSON string below
json = "{}"
# create an instance of ServiceInstance from a JSON string
service_instance_instance = ServiceInstance.from_json(json)
# print the JSON string representation of the object
print(ServiceInstance.to_json())

# convert the object into a dict
service_instance_dict = service_instance_instance.to_dict()
# create an instance of ServiceInstance from a dict
service_instance_from_dict = ServiceInstance.from_dict(service_instance_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


