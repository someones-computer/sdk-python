# SealedSecret


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**algo** | **str** |  | [optional] 
**key_id** | **str** |  | [optional] 
**nonce** | **str** |  | [optional] 
**ciphertext** | **str** |  | [optional] 

## Example

```python
from someones_computer_sdk.models.sealed_secret import SealedSecret

# TODO update the JSON string below
json = "{}"
# create an instance of SealedSecret from a JSON string
sealed_secret_instance = SealedSecret.from_json(json)
# print the JSON string representation of the object
print(SealedSecret.to_json())

# convert the object into a dict
sealed_secret_dict = sealed_secret_instance.to_dict()
# create an instance of SealedSecret from a dict
sealed_secret_from_dict = SealedSecret.from_dict(sealed_secret_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


