# SwarmNode


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**swarm** | **str** |  | [optional] 
**node_id** | **str** | The swarm-assigned node id. | [optional] 
**hostname** | **str** |  | [optional] 
**state** | **str** |  | [optional] 
**capacity** | **Dict[str, Optional[str]]** | This node&#39;s share of the cluster&#39;s capacity, as the reconciler read it. | [optional] 
**id** | **str** |  | [optional] [readonly] 
**created_at** | **datetime** |  | [optional] [readonly] 
**updated_at** | **datetime** |  | [optional] [readonly] 

## Example

```python
from someones_computer_sdk.models.swarm_node import SwarmNode

# TODO update the JSON string below
json = "{}"
# create an instance of SwarmNode from a JSON string
swarm_node_instance = SwarmNode.from_json(json)
# print the JSON string representation of the object
print(SwarmNode.to_json())

# convert the object into a dict
swarm_node_dict = swarm_node_instance.to_dict()
# create an instance of SwarmNode from a dict
swarm_node_from_dict = SwarmNode.from_dict(swarm_node_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


