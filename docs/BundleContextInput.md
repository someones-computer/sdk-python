# BundleContextInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**service** | **str** |  | [default to '']
**context_sha256** | **str** |  | [default to '']
**dockerfile** | **str** |  | [optional] [default to 'Dockerfile']
**additional_contexts** | [**List[BundleAdditionalContextInput]**](BundleAdditionalContextInput.md) |  | [optional] 

## Example

```python
from someones_computer_sdk.models.bundle_context_input import BundleContextInput

# TODO update the JSON string below
json = "{}"
# create an instance of BundleContextInput from a JSON string
bundle_context_input_instance = BundleContextInput.from_json(json)
# print the JSON string representation of the object
print(BundleContextInput.to_json())

# convert the object into a dict
bundle_context_input_dict = bundle_context_input_instance.to_dict()
# create an instance of BundleContextInput from a dict
bundle_context_input_from_dict = BundleContextInput.from_dict(bundle_context_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


