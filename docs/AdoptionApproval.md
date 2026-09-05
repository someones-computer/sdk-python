# AdoptionApproval

A human's decision on one compose service the adoption planner detected — approve it, or decline it (§15).  **The switch arms detection; this is what authorizes the act.** {@see \\App\\Service\\ManagedService\\Adoption\\AdoptionReconciler} only ever turns a candidate into a real {@see ManagedService}/{@see ServiceBinding} pair when a row here says `approved`, and only for the compose service name recorded — a rename is a different candidate with no decision of its own yet.  **There is no \"pending\" row.** A service the planner reports and nobody has decided on simply has none here; recording one for every candidate on every deploy would need cleaning up the moment a service is renamed away, for a state (\"undecided\") a missing row already expresses for free.  One row per (application, compose service): deciding again — approving after a rejection, or the reverse — updates it rather than accumulating history, because only the current decision governs what the next deploy does.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**application** | **str** |  | [optional] 
**compose_service_name** | **str** | The compose service name this decision is about — joined against a live plan by name. | [optional] 
**approved** | **bool** |  | [optional] 
**decided_at** | **datetime** |  | [optional] 
**id** | **str** |  | [optional] [readonly] 

## Example

```python
from someones_computer_sdk.models.adoption_approval import AdoptionApproval

# TODO update the JSON string below
json = "{}"
# create an instance of AdoptionApproval from a JSON string
adoption_approval_instance = AdoptionApproval.from_json(json)
# print the JSON string representation of the object
print(AdoptionApproval.to_json())

# convert the object into a dict
adoption_approval_dict = adoption_approval_instance.to_dict()
# create an instance of AdoptionApproval from a dict
adoption_approval_from_dict = AdoptionApproval.from_dict(adoption_approval_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


