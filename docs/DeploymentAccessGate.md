# DeploymentAccessGate

List an application's per-deployment access-gate overrides.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**application** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**access_gate** | **str** |  | [optional] [default to 'none']
**id** | **str** |  | [optional] [readonly] 
**created_at** | **datetime** |  | [optional] [readonly] 
**updated_at** | **datetime** |  | [optional] [readonly] 
**access_gate_credential** | [**SealedSecret**](SealedSecret.md) |  | [optional] 

## Example

```python
from someones_computer_sdk.models.deployment_access_gate import DeploymentAccessGate

# TODO update the JSON string below
json = "{}"
# create an instance of DeploymentAccessGate from a JSON string
deployment_access_gate_instance = DeploymentAccessGate.from_json(json)
# print the JSON string representation of the object
print(DeploymentAccessGate.to_json())

# convert the object into a dict
deployment_access_gate_dict = deployment_access_gate_instance.to_dict()
# create an instance of DeploymentAccessGate from a dict
deployment_access_gate_from_dict = DeploymentAccessGate.from_dict(deployment_access_gate_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


