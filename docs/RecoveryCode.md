# RecoveryCode


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**user** | [**User**](User.md) |  | [optional] 
**code_hash** | **str** | SHA-256 hex digest of the plaintext code; the only copy that is ever stored. | [optional] 
**used_at** | **datetime** | When this code was spent; null means it is still usable. | [optional] [readonly] 
**id** | **str** |  | [optional] [readonly] 
**created_at** | **datetime** |  | [optional] [readonly] 
**updated_at** | **datetime** |  | [optional] [readonly] 
**used** | **bool** |  | [optional] [readonly] 

## Example

```python
from someones_computer_sdk.models.recovery_code import RecoveryCode

# TODO update the JSON string below
json = "{}"
# create an instance of RecoveryCode from a JSON string
recovery_code_instance = RecoveryCode.from_json(json)
# print the JSON string representation of the object
print(RecoveryCode.to_json())

# convert the object into a dict
recovery_code_dict = recovery_code_instance.to_dict()
# create an instance of RecoveryCode from a dict
recovery_code_from_dict = RecoveryCode.from_dict(recovery_code_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


