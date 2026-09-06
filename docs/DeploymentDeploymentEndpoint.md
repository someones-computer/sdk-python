# DeploymentDeploymentEndpoint

An IMMUTABLE compose revision. A deploy is a new row; rollback re-points Application::$currentDeployment at an older one. Placement is resolved onto this row (targetSwarm) at deploy time, so migration is just the next revision.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**service** | **str** |  | [optional] 
**protocol** | **str** |  | [optional] 
**host** | **str** |  | [optional] 
**port** | **int** |  | [optional] 
**target_port** | **int** |  | [optional] 
**assigned** | **bool** |  | [optional] 
**edge_routed** | **bool** |  | [optional] 
**url** | **str** |  | [optional] 
**host_unknown_reason** | **str** |  | [optional] 

## Example

```python
from someones_computer_sdk.models.deployment_deployment_endpoint import DeploymentDeploymentEndpoint

# TODO update the JSON string below
json = "{}"
# create an instance of DeploymentDeploymentEndpoint from a JSON string
deployment_deployment_endpoint_instance = DeploymentDeploymentEndpoint.from_json(json)
# print the JSON string representation of the object
print(DeploymentDeploymentEndpoint.to_json())

# convert the object into a dict
deployment_deployment_endpoint_dict = deployment_deployment_endpoint_instance.to_dict()
# create an instance of DeploymentDeploymentEndpoint from a dict
deployment_deployment_endpoint_from_dict = DeploymentDeploymentEndpoint.from_dict(deployment_deployment_endpoint_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


