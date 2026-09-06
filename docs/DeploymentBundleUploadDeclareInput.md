# DeploymentBundleUploadDeclareInput

An IMMUTABLE compose revision. A deploy is a new row; rollback re-points Application::$currentDeployment at an older one. Placement is resolved onto this row (targetSwarm) at deploy time, so migration is just the next revision.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**application** | **str** |  | 
**client** | **str** | Matches &#x60;App\\Service\\Bundle\\BundleManifest::$client&#x60; — which client produced this. | [default to 'api']
**name** | **str** |  | [optional] 
**force** | **bool** | Ask for a new revision even if this digest already matches one — {@see BundleManifest::$force}&#39;s own meaning, unchanged. | [optional] [default to False]
**compose** | **str** |  | [default to '']
**contexts** | [**List[BundleContextInput]**](BundleContextInput.md) |  | [optional] 
**images** | [**List[BundleForwardedImageInput]**](BundleForwardedImageInput.md) |  | [optional] 

## Example

```python
from someones_computer_sdk.models.deployment_bundle_upload_declare_input import DeploymentBundleUploadDeclareInput

# TODO update the JSON string below
json = "{}"
# create an instance of DeploymentBundleUploadDeclareInput from a JSON string
deployment_bundle_upload_declare_input_instance = DeploymentBundleUploadDeclareInput.from_json(json)
# print the JSON string representation of the object
print(DeploymentBundleUploadDeclareInput.to_json())

# convert the object into a dict
deployment_bundle_upload_declare_input_dict = deployment_bundle_upload_declare_input_instance.to_dict()
# create an instance of DeploymentBundleUploadDeclareInput from a dict
deployment_bundle_upload_declare_input_from_dict = DeploymentBundleUploadDeclareInput.from_dict(deployment_bundle_upload_declare_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


