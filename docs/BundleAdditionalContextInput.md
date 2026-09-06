# BundleAdditionalContextInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [default to '']
**context_sha256** | **str** |  | [default to '']

## Example

```python
from someones_computer_sdk.models.bundle_additional_context_input import BundleAdditionalContextInput

# TODO update the JSON string below
json = "{}"
# create an instance of BundleAdditionalContextInput from a JSON string
bundle_additional_context_input_instance = BundleAdditionalContextInput.from_json(json)
# print the JSON string representation of the object
print(BundleAdditionalContextInput.to_json())

# convert the object into a dict
bundle_additional_context_input_dict = bundle_additional_context_input_instance.to_dict()
# create an instance of BundleAdditionalContextInput from a dict
bundle_additional_context_input_from_dict = BundleAdditionalContextInput.from_dict(bundle_additional_context_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


