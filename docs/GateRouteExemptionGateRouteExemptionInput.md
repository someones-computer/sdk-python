# GateRouteExemptionGateRouteExemptionInput

Approve one route that the current revision declares as exempt from the access gate.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**application** | **str** |  | 
**service_name** | **str** |  | [default to '']
**host** | **str** |  | [default to '']
**path_prefix** | **str** |  | [default to '']

## Example

```python
from someones_computer_sdk.models.gate_route_exemption_gate_route_exemption_input import GateRouteExemptionGateRouteExemptionInput

# TODO update the JSON string below
json = "{}"
# create an instance of GateRouteExemptionGateRouteExemptionInput from a JSON string
gate_route_exemption_gate_route_exemption_input_instance = GateRouteExemptionGateRouteExemptionInput.from_json(json)
# print the JSON string representation of the object
print(GateRouteExemptionGateRouteExemptionInput.to_json())

# convert the object into a dict
gate_route_exemption_gate_route_exemption_input_dict = gate_route_exemption_gate_route_exemption_input_instance.to_dict()
# create an instance of GateRouteExemptionGateRouteExemptionInput from a dict
gate_route_exemption_gate_route_exemption_input_from_dict = GateRouteExemptionGateRouteExemptionInput.from_dict(gate_route_exemption_gate_route_exemption_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


