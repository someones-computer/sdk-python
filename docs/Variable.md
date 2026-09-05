# Variable


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**organization** | **str** | Re-home this variable. Used only when an application-scoped row follows its {@see Application} across organizations — an org-shared row (&#x60;$application &#x3D;&#x3D;&#x3D; null&#x60;) has no application to follow and is never moved this way. | [optional] 
**application** | **str** | Null &#x3D;&gt; org-shared across all of the organization&#39;s applications. | [optional] 
**key** | **str** | The environment variable name. (\&quot;key\&quot; is reserved in some SQL dialects.) | [optional] 
**sensitive** | **bool** |  | [optional] [default to False]
**secret_file_delivery** | **bool** | Opt-in only, and meaningless unless {@see $sensitive} is also true: whether this secret is delivered to its containers as a mounted Swarm secret file (plus a &#x60;&lt;KEY&gt;_FILE&#x60; env var naming its path) rather than as a plain &#x60;Env&#x60; entry — {@see \\App\\Service\\Deploy\\StackDeployer}. | [optional] [default to False]
**versions** | [**List[VariableVersion]**](VariableVersion.md) |  | [optional] 
**id** | **str** |  | [optional] [readonly] 
**deleted_at** | **datetime** |  | [optional] [readonly] 
**created_at** | **datetime** |  | [optional] [readonly] 
**updated_at** | **datetime** |  | [optional] [readonly] 
**org_shared** | **bool** |  | [optional] [readonly] 
**deleted** | **bool** |  | [optional] [readonly] 

## Example

```python
from someones_computer_sdk.models.variable import Variable

# TODO update the JSON string below
json = "{}"
# create an instance of Variable from a JSON string
variable_instance = Variable.from_json(json)
# print the JSON string representation of the object
print(Variable.to_json())

# convert the object into a dict
variable_dict = variable_instance.to_dict()
# create an instance of Variable from a dict
variable_from_dict = Variable.from_dict(variable_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


