# BundleUploadTarget


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**service** | **str** |  | [optional] 
**name** | **str** | The additional context&#39;s name, or null for a service&#39;s own primary context/image. | [optional] 
**context_sha256** | **str** |  | [optional] 
**already_stored** | **bool** |  | [optional] 
**upload_url** | **str** |  | [optional] 

## Example

```python
from someones_computer_sdk.models.bundle_upload_target import BundleUploadTarget

# TODO update the JSON string below
json = "{}"
# create an instance of BundleUploadTarget from a JSON string
bundle_upload_target_instance = BundleUploadTarget.from_json(json)
# print the JSON string representation of the object
print(BundleUploadTarget.to_json())

# convert the object into a dict
bundle_upload_target_dict = bundle_upload_target_instance.to_dict()
# create an instance of BundleUploadTarget from a dict
bundle_upload_target_from_dict = BundleUploadTarget.from_dict(bundle_upload_target_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


