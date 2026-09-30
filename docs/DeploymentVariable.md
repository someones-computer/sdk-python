# DeploymentVariable


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**deployment** | **str** |  | [optional] 
**variable_version** | [**VariableVersion**](VariableVersion.md) |  | [optional] 
**id** | **str** |  | [optional] [readonly] 
**key** | **str** | The environment variable name this entry contributes. | [optional] [readonly] 

## Example

```python
from someones_computer_sdk.models.deployment_variable import DeploymentVariable

# TODO update the JSON string below
json = "{}"
# create an instance of DeploymentVariable from a JSON string
deployment_variable_instance = DeploymentVariable.from_json(json)
# print the JSON string representation of the object
print(DeploymentVariable.to_json())

# convert the object into a dict
deployment_variable_dict = deployment_variable_instance.to_dict()
# create an instance of DeploymentVariable from a dict
deployment_variable_from_dict = DeploymentVariable.from_dict(deployment_variable_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


