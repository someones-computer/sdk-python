# VariableVersion


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**variable** | [**Variable**](Variable.md) |  | [optional] 
**version** | **int** |  | [optional] 
**algo** | **str** | Encryption algorithm identifier, e.g. \&quot;xsalsa20poly1305\&quot;. Sensitive only. | [optional] [readonly] 
**key_id** | **str** | Identifier of the key-encryption-key that wrapped this value. Sensitive only. | [optional] [readonly] 
**nonce** | **str** |  | [optional] [readonly] 
**ciphertext** | **str** |  | [optional] [readonly] 
**created_at** | **datetime** |  | [optional] [readonly] 
**created_by** | [**User**](User.md) |  | [optional] 
**id** | **str** |  | [optional] [readonly] 
**encrypted** | **str** | Populate an encrypted (sensitive) value. | [optional] 
**plaintext** | **str** | Populate a plaintext (non-sensitive) value. | [optional] 

## Example

```python
from someones_computer_sdk.models.variable_version import VariableVersion

# TODO update the JSON string below
json = "{}"
# create an instance of VariableVersion from a JSON string
variable_version_instance = VariableVersion.from_json(json)
# print the JSON string representation of the object
print(VariableVersion.to_json())

# convert the object into a dict
variable_version_dict = variable_version_instance.to_dict()
# create an instance of VariableVersion from a dict
variable_version_from_dict = VariableVersion.from_dict(variable_version_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


