# AdoptionApprovalAdoptionApprovalInput

Approve or decline an adopted compose service candidate.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**application** | **str** |  | 
**compose_service_name** | **str** |  | [default to '']
**approved** | **bool** |  | [optional] [default to False]

## Example

```python
from someones_computer_sdk.models.adoption_approval_adoption_approval_input import AdoptionApprovalAdoptionApprovalInput

# TODO update the JSON string below
json = "{}"
# create an instance of AdoptionApprovalAdoptionApprovalInput from a JSON string
adoption_approval_adoption_approval_input_instance = AdoptionApprovalAdoptionApprovalInput.from_json(json)
# print the JSON string representation of the object
print(AdoptionApprovalAdoptionApprovalInput.to_json())

# convert the object into a dict
adoption_approval_adoption_approval_input_dict = adoption_approval_adoption_approval_input_instance.to_dict()
# create an instance of AdoptionApprovalAdoptionApprovalInput from a dict
adoption_approval_adoption_approval_input_from_dict = AdoptionApprovalAdoptionApprovalInput.from_dict(adoption_approval_adoption_approval_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


