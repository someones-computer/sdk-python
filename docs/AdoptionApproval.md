# AdoptionApproval

List adoption approval decisions the caller can see.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**application** | **str** |  | [optional] 
**compose_service_name** | **str** | The compose service name this decision is about — joined against a live plan by name. | [optional] 
**approved** | **bool** |  | [optional] 
**decided_at** | **datetime** |  | [optional] 
**id** | **str** |  | [optional] [readonly] 

## Example

```python
from someones_computer_sdk.models.adoption_approval import AdoptionApproval

# TODO update the JSON string below
json = "{}"
# create an instance of AdoptionApproval from a JSON string
adoption_approval_instance = AdoptionApproval.from_json(json)
# print the JSON string representation of the object
print(AdoptionApproval.to_json())

# convert the object into a dict
adoption_approval_dict = adoption_approval_instance.to_dict()
# create an instance of AdoptionApproval from a dict
adoption_approval_from_dict = AdoptionApproval.from_dict(adoption_approval_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


