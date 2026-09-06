# BundleForwardedImageInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**service** | **str** |  | [default to '']
**image** | **str** |  | [default to '']
**context_sha256** | **str** |  | [default to '']

## Example

```python
from someones_computer_sdk.models.bundle_forwarded_image_input import BundleForwardedImageInput

# TODO update the JSON string below
json = "{}"
# create an instance of BundleForwardedImageInput from a JSON string
bundle_forwarded_image_input_instance = BundleForwardedImageInput.from_json(json)
# print the JSON string representation of the object
print(BundleForwardedImageInput.to_json())

# convert the object into a dict
bundle_forwarded_image_input_dict = bundle_forwarded_image_input_instance.to_dict()
# create an instance of BundleForwardedImageInput from a dict
bundle_forwarded_image_input_from_dict = BundleForwardedImageInput.from_dict(bundle_forwarded_image_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


