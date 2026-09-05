# Membership


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**organization** | **str** |  | [optional] 
**user** | [**User**](User.md) |  | [optional] 
**role** | **str** |  | [optional] 
**id** | **str** |  | [optional] [readonly] 
**created_at** | **datetime** |  | [optional] [readonly] 
**updated_at** | **datetime** |  | [optional] [readonly] 

## Example

```python
from someones_computer_sdk.models.membership import Membership

# TODO update the JSON string below
json = "{}"
# create an instance of Membership from a JSON string
membership_instance = Membership.from_json(json)
# print the JSON string representation of the object
print(Membership.to_json())

# convert the object into a dict
membership_dict = membership_instance.to_dict()
# create an instance of Membership from a dict
membership_from_dict = Membership.from_dict(membership_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


