# DeploymentBundleUploadConfirmOutput

An IMMUTABLE compose revision. A deploy is a new row; rollback re-points Application::$currentDeployment at an older one. Placement is resolved onto this row (targetSwarm) at deploy time, so migration is just the next revision.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**sequence** | **int** |  | [optional] 
**status** | **str** |  | [optional] 
**digest** | **str** |  | [optional] 
**url** | **str** |  | [optional] 
**retried** | **bool** | True when this upload restarted an existing failed revision rather than minting one. | [optional] 
**warning** | **str** | A deploy this organization can still afford, but is projected to run out of paying for soon — null on every ordinary deploy. | [optional] 

## Example

```python
from someones_computer_sdk.models.deployment_bundle_upload_confirm_output import DeploymentBundleUploadConfirmOutput

# TODO update the JSON string below
json = "{}"
# create an instance of DeploymentBundleUploadConfirmOutput from a JSON string
deployment_bundle_upload_confirm_output_instance = DeploymentBundleUploadConfirmOutput.from_json(json)
# print the JSON string representation of the object
print(DeploymentBundleUploadConfirmOutput.to_json())

# convert the object into a dict
deployment_bundle_upload_confirm_output_dict = deployment_bundle_upload_confirm_output_instance.to_dict()
# create an instance of DeploymentBundleUploadConfirmOutput from a dict
deployment_bundle_upload_confirm_output_from_dict = DeploymentBundleUploadConfirmOutput.from_dict(deployment_bundle_upload_confirm_output_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


