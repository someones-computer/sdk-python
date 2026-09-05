# OAuthIdentity


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**provider** | **str** |  | [optional] 
**provider_user_id** | **str** | The stable, provider-assigned user id (never the email). | [optional] 
**user** | [**User**](User.md) |  | [optional] 
**id** | **str** |  | [optional] [readonly] 
**created_at** | **datetime** |  | [optional] [readonly] 
**updated_at** | **datetime** |  | [optional] [readonly] 

## Example

```python
from someones_computer_sdk.models.o_auth_identity import OAuthIdentity

# TODO update the JSON string below
json = "{}"
# create an instance of OAuthIdentity from a JSON string
o_auth_identity_instance = OAuthIdentity.from_json(json)
# print the JSON string representation of the object
print(OAuthIdentity.to_json())

# convert the object into a dict
o_auth_identity_dict = o_auth_identity_instance.to_dict()
# create an instance of OAuthIdentity from a dict
o_auth_identity_from_dict = OAuthIdentity.from_dict(o_auth_identity_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


