# DeploymentBundleUploadDeclareOutput

Declare a bundle upload and get a presigned URL to upload it to.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**contexts** | [**List[BundleUploadTarget]**](BundleUploadTarget.md) |  | [optional] 
**additional_contexts** | [**List[BundleUploadTarget]**](BundleUploadTarget.md) |  | [optional] 
**images** | [**List[BundleUploadTarget]**](BundleUploadTarget.md) |  | [optional] 
**expires_at** | **datetime** |  | [optional] 

## Example

```python
from someones_computer_sdk.models.deployment_bundle_upload_declare_output import DeploymentBundleUploadDeclareOutput

# TODO update the JSON string below
json = "{}"
# create an instance of DeploymentBundleUploadDeclareOutput from a JSON string
deployment_bundle_upload_declare_output_instance = DeploymentBundleUploadDeclareOutput.from_json(json)
# print the JSON string representation of the object
print(DeploymentBundleUploadDeclareOutput.to_json())

# convert the object into a dict
deployment_bundle_upload_declare_output_dict = deployment_bundle_upload_declare_output_instance.to_dict()
# create an instance of DeploymentBundleUploadDeclareOutput from a dict
deployment_bundle_upload_declare_output_from_dict = DeploymentBundleUploadDeclareOutput.from_dict(deployment_bundle_upload_declare_output_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


