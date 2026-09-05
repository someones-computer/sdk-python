# OrganizationJsonMergePatch

Ownership and (future) billing boundary. Owns applications, may own BYO swarms.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**machine_account** | [**User**](User.md) |  | [optional] 
**name** | **str** |  | [optional] 
**slug** | **str** | &#x60;unique: true&#x60; stops two organizations holding the same *string*; the constraint stops two holding strings that fold to the same **stack name**, which the database has no way to express (#860). Both are needed: the column guards the identifier, the constraint guards what is derived from it. | [optional] 
**theme** | **str** | The skin this organization&#39;s members see, or null to take the instance&#39;s. | [optional] 
**tier_pin** | **str** | An operator&#39;s grant of a tier this organization would not reach through any member — {@see \\App\\Enum\\AccountTier::Verified} in particular, which is granted rather than earned and belongs to a contractual relationship with the *organization*, not incidentally to whichever of its members happens to carry the highest personal tier ({@see \\App\\Service\\Trust\\TierResolver::forOrganization()}). A member individually pinned &#x60;Verified&#x60; still lifts the org the same way a &#x60;Trusted&#x60; member always has — this pin is for granting it to the org directly, without needing a person to hang it on. | [optional] [readonly] 
**tier_pinned_at** | **datetime** |  | [optional] [readonly] 
**tier_pinned_by** | [**User**](User.md) |  | [optional] 
**tier_pin_reason** | **str** |  | [optional] [readonly] 
**low_balance_warned_at** | **datetime** | When {@see \\App\\MessageHandler\\CheckRunwayHandler} last warned this organization that its projected runway had dropped below the threshold; null once no warning is outstanding. Set once per crossing and cleared the moment the projection recovers — by a top-up or by the burn easing off — which is what makes \&quot;warn once, re-arm on recovery\&quot; a fact this column can answer rather than something re-derived from the notification table on every tick. | [optional] [readonly] 
**two_factor_required_at** | **datetime** | When an Owner/Admin turned on the requirement that every member of this organization protects their account with a second factor; null means it is optional. A reversible policy toggle, stamped like {@see User::$disabledAt} rather than a verdict, so no \&quot;who set it\&quot; attribution. | [optional] [readonly] 
**memberships** | [**List[Membership]**](Membership.md) |  | [optional] 
**applications** | **List[str]** |  | [optional] 
**swarms** | **List[str]** | BYO swarms owned by this organization. | [optional] 
**machines** | [**List[Machine]**](Machine.md) |  | [optional] 
**credit_transactions** | **List[str]** | The append-only credit ledger. | [optional] 
**variables** | [**List[Variable]**](Variable.md) |  | [optional] 
**signals** | [**List[OrganizationSignal]**](OrganizationSignal.md) |  | [optional] 
**id** | **str** |  | [optional] [readonly] 
**deleted_at** | **datetime** |  | [optional] [readonly] 
**created_at** | **datetime** |  | [optional] [readonly] 
**updated_at** | **datetime** |  | [optional] [readonly] 
**tier_pinned** | **bool** |  | [optional] [readonly] 
**deleted** | **bool** |  | [optional] [readonly] 

## Example

```python
from someones_computer_sdk.models.organization_json_merge_patch import OrganizationJsonMergePatch

# TODO update the JSON string below
json = "{}"
# create an instance of OrganizationJsonMergePatch from a JSON string
organization_json_merge_patch_instance = OrganizationJsonMergePatch.from_json(json)
# print the JSON string representation of the object
print(OrganizationJsonMergePatch.to_json())

# convert the object into a dict
organization_json_merge_patch_dict = organization_json_merge_patch_instance.to_dict()
# create an instance of OrganizationJsonMergePatch from a dict
organization_json_merge_patch_from_dict = OrganizationJsonMergePatch.from_dict(organization_json_merge_patch_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


