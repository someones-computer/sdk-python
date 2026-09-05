# Failure


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**deployment** | **str** | Deleting a revision deletes its failures with it. They are an account of what that revision did, and outliving the thing they describe would leave a page that can only render half of itself. | [optional] 
**proxmox_instance** | [**ProxmoxInstance**](ProxmoxInstance.md) |  | [optional] 
**phase** | **str** |  | [optional] 
**reason** | **str** | Verbatim, as it was written to &#x60;Deployment::$statusReason&#x60; at the time. | [optional] 
**reference** | **str** | The short handle this failure is quoted by — see {@see FailureReference}. | [optional] [readonly] 
**service** | **str** | Which compose service, where the phase happens per-service. Null for the phases that fail the revision as a whole (placement, stranded) and for a deploy that never got as far as naming one. | [optional] 
**build_log_key** | **str** | Object key of the build log as it stood, or null when there was none. | [optional] 
**image_digest** | **str** | The digest a {@see FailurePhase::Scan} failure was quarantined over — null for every other phase. What lets the scan quarantine queue (docs/image-scanning.md, #816) resolve straight from a quarantined revision to the exact {@see \\App\\Entity\\ImageScan} an operator&#39;s Clear or Uphold acts on, without re-deriving it from a pinned image reference or a reason string meant for a person to read. | [optional] 
**share_token** | **str** | The capability that makes {@see \\App\\Controller\\FailureController::shared()} serve this to someone with no session, or null while it is private. | [optional] [readonly] 
**shared_at** | **datetime** |  | [optional] [readonly] 
**share_expires_at** | **datetime** | When the capability above stops working, 24 hours after it was minted. | [optional] [readonly] 
**shared_by** | [**User**](User.md) |  | [optional] 
**id** | **str** |  | [optional] [readonly] 
**created_at** | **datetime** |  | [optional] [readonly] 
**updated_at** | **datetime** |  | [optional] [readonly] 
**display_label** | **str** | The reference as it is written for a reader: &#x60;F-24GT1BQ7&#x60;. | [optional] [readonly] 
**shared** | **bool** | Whether an unauthenticated request may read this: a token was minted and it has not yet passed its expiry. | [optional] [readonly] 

## Example

```python
from someones_computer_sdk.models.failure import Failure

# TODO update the JSON string below
json = "{}"
# create an instance of Failure from a JSON string
failure_instance = Failure.from_json(json)
# print the JSON string representation of the object
print(Failure.to_json())

# convert the object into a dict
failure_dict = failure_instance.to_dict()
# create an instance of Failure from a dict
failure_from_dict = Failure.from_dict(failure_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


