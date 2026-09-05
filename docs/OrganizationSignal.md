# OrganizationSignal


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**organization** | **str** |  | [optional] 
**application** | **str** | Which application&#39;s compose file produced it — deleting the application does not un-say what it asked for. | [optional] 
**reason** | **str** | Verbatim, as {@see \\App\\Service\\Compose\\ComposeParser::parse()} produced it. | [optional] 
**id** | **str** |  | [optional] [readonly] 
**created_at** | **datetime** |  | [optional] [readonly] 
**updated_at** | **datetime** |  | [optional] [readonly] 

## Example

```python
from someones_computer_sdk.models.organization_signal import OrganizationSignal

# TODO update the JSON string below
json = "{}"
# create an instance of OrganizationSignal from a JSON string
organization_signal_instance = OrganizationSignal.from_json(json)
# print the JSON string representation of the object
print(OrganizationSignal.to_json())

# convert the object into a dict
organization_signal_dict = organization_signal_instance.to_dict()
# create an instance of OrganizationSignal from a dict
organization_signal_from_dict = OrganizationSignal.from_dict(organization_signal_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


