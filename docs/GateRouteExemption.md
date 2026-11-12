# GateRouteExemption

List the access-gate route exemptions the caller can see.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**application** | **str** |  | [optional] 
**service_name** | **str** |  | [optional] 
**host** | **str** |  | [optional] [readonly] 
**path_prefix** | **str** |  | [optional] [readonly] 
**methods** | **str** | Comma-joined, sorted verbs: {@see GateExemption::methodsKey()}. | [optional] [readonly] 
**approved_at** | **datetime** |  | [optional] 
**id** | **UUID** |  | [optional] [readonly] 

## Example

```python
from someones_computer_sdk.models.gate_route_exemption import GateRouteExemption

# TODO update the JSON string below
json = "{}"
# create an instance of GateRouteExemption from a JSON string
gate_route_exemption_instance = GateRouteExemption.from_json(json)
# print the JSON string representation of the object
print(GateRouteExemption.to_json())

# convert the object into a dict
gate_route_exemption_dict = gate_route_exemption_instance.to_dict()
# create an instance of GateRouteExemption from a dict
gate_route_exemption_from_dict = GateRouteExemption.from_dict(gate_route_exemption_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


