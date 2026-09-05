# AdoptionApprovalAdoptionApprovalInput

A human's decision on one compose service the adoption planner detected — approve it, or decline it (§15).  **The switch arms detection; this is what authorizes the act.** {@see \\App\\Service\\ManagedService\\Adoption\\AdoptionReconciler} only ever turns a candidate into a real {@see ManagedService}/{@see ServiceBinding} pair when a row here says `approved`, and only for the compose service name recorded — a rename is a different candidate with no decision of its own yet.  **There is no \"pending\" row.** A service the planner reports and nobody has decided on simply has none here; recording one for every candidate on every deploy would need cleaning up the moment a service is renamed away, for a state (\"undecided\") a missing row already expresses for free.  One row per (application, compose service): deciding again — approving after a rejection, or the reverse — updates it rather than accumulating history, because only the current decision governs what the next deploy does.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**application** | **str** |  | 
**compose_service_name** | **str** |  | [default to '']
**approved** | **bool** |  | [optional] [default to False]

## Example

```python
from someones_computer_sdk.models.adoption_approval_adoption_approval_input import AdoptionApprovalAdoptionApprovalInput

# TODO update the JSON string below
json = "{}"
# create an instance of AdoptionApprovalAdoptionApprovalInput from a JSON string
adoption_approval_adoption_approval_input_instance = AdoptionApprovalAdoptionApprovalInput.from_json(json)
# print the JSON string representation of the object
print(AdoptionApprovalAdoptionApprovalInput.to_json())

# convert the object into a dict
adoption_approval_adoption_approval_input_dict = adoption_approval_adoption_approval_input_instance.to_dict()
# create an instance of AdoptionApprovalAdoptionApprovalInput from a dict
adoption_approval_adoption_approval_input_from_dict = AdoptionApprovalAdoptionApprovalInput.from_dict(adoption_approval_adoption_approval_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


