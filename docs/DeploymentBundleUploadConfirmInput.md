# DeploymentBundleUploadConfirmInput

An IMMUTABLE compose revision. A deploy is a new row; rollback re-points Application::$currentDeployment at an older one. Placement is resolved onto this row (targetSwarm) at deploy time, so migration is just the next revision.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**secrets** | **Dict[str, Dict[str, str]]** | Raw &#x60;build.secrets&#x60; values, keyed by service then by BuildKit secret id (Grey.ooo/someones.computer_agent#46) — matches &#x60;App\\Service\\Bundle\\BundleIngestor::commitFromStoredContent()&#x60;&#39;s &#x60;$secrets&#x60; parameter. | [optional] 
**application** | **str** |  | 
**client** | **str** | Matches &#x60;App\\Service\\Bundle\\BundleManifest::$client&#x60; — which client produced this. | [default to 'api']
**name** | **str** |  | [optional] 
**force** | **bool** | Ask for a new revision even if this digest already matches one — {@see BundleManifest::$force}&#39;s own meaning, unchanged. | [optional] [default to False]
**compose** | **str** |  | [default to '']
**contexts** | [**List[BundleContextInput]**](BundleContextInput.md) |  | [optional] 
**images** | [**List[BundleForwardedImageInput]**](BundleForwardedImageInput.md) |  | [optional] 

## Example

```python
from someones_computer_sdk.models.deployment_bundle_upload_confirm_input import DeploymentBundleUploadConfirmInput

# TODO update the JSON string below
json = "{}"
# create an instance of DeploymentBundleUploadConfirmInput from a JSON string
deployment_bundle_upload_confirm_input_instance = DeploymentBundleUploadConfirmInput.from_json(json)
# print the JSON string representation of the object
print(DeploymentBundleUploadConfirmInput.to_json())

# convert the object into a dict
deployment_bundle_upload_confirm_input_dict = deployment_bundle_upload_confirm_input_instance.to_dict()
# create an instance of DeploymentBundleUploadConfirmInput from a dict
deployment_bundle_upload_confirm_input_from_dict = DeploymentBundleUploadConfirmInput.from_dict(deployment_bundle_upload_confirm_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


