# PortAllocation


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**swarm** | **str** | The cluster this port is claimed on. Deleting the cluster takes its allocations with it — a reservation on a swarm that no longer exists is not holding anything back. | [optional] 
**application** | **str** |  | [optional] 
**deployment_name** | **str** | The deployment name this reservation belongs to — {@see Deployment::$name}, or &#x60;&#39;&#39;&#x60; for a revision that carries no name (before the field existed, or a client that never sent one), which is its own stable scope rather than a wildcard: every unnamed revision of an application shares it, exactly the single continuous scope every application had before this column existed. | [optional] 
**service_name** | **str** | The compose service name, as the customer&#39;s file spells it. | [optional] 
**target_port** | **int** | The container port traffic is forwarded to. | [optional] 
**protocol** | **str** |  | [optional] 
**published_port** | **int** | What the world connects to. Unique per protocol on this cluster. | [optional] 
**assigned** | **bool** | Whether the platform chose this number or the compose file did. | [optional] 
**id** | **str** |  | [optional] [readonly] 
**created_at** | **datetime** |  | [optional] [readonly] 
**updated_at** | **datetime** |  | [optional] [readonly] 

## Example

```python
from someones_computer_sdk.models.port_allocation import PortAllocation

# TODO update the JSON string below
json = "{}"
# create an instance of PortAllocation from a JSON string
port_allocation_instance = PortAllocation.from_json(json)
# print the JSON string representation of the object
print(PortAllocation.to_json())

# convert the object into a dict
port_allocation_dict = port_allocation_instance.to_dict()
# create an instance of PortAllocation from a dict
port_allocation_from_dict = PortAllocation.from_dict(port_allocation_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


