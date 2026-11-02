# Organization

List organizations the caller is a member of.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**machine_account** | [**User**](User.md) | The principal an {@see OrganizationToken} authenticates as: a machine account this platform owns, not a person. | [optional] 
**name** | **str** |  | [optional] 
**slug** | **str** | &#x60;unique: true&#x60; stops two organizations holding the same *string*; the constraint stops two holding strings that fold to the same **stack name**, which the database has no way to express (#860). Both are needed: the column guards the identifier, the constraint guards what is derived from it. | [optional] 
**theme** | **str** | The skin this organization&#39;s members see, or null to take the instance&#39;s. | [optional] 
**tier_pin** | **str** | An operator&#39;s grant of a tier this organization would not reach through any member — {@see \\App\\Enum\\AccountTier::Verified} in particular, which is granted rather than earned and belongs to a contractual relationship with the *organization*, not incidentally to whichever of its members happens to carry the highest personal tier ({@see \\App\\Service\\Trust\\TierResolver::forOrganization()}). A member individually pinned &#x60;Verified&#x60; still lifts the org the same way a &#x60;Trusted&#x60; member always has — this pin is for granting it to the org directly, without needing a person to hang it on. | [optional] [readonly] 
**tier_pinned_at** | **datetime** |  | [optional] [readonly] 
**tier_pinned_by** | [**User**](User.md) | Nullable and SET NULL: somebody can delete an operator, and the pin outlives them. | [optional] [readonly] 
**tier_pin_reason** | **str** |  | [optional] [readonly] 
**low_balance_warned_at** | **datetime** | When {@see \\App\\MessageHandler\\CheckRunwayHandler} last warned this organization that its projected runway had dropped below the threshold; null once no warning is outstanding. Set once per crossing and cleared the moment the projection recovers — by a top-up or by the burn easing off — which is what makes \&quot;warn once, re-arm on recovery\&quot; a fact this column can answer rather than something re-derived from the notification table on every tick. | [optional] [readonly] 
**two_factor_required_at** | **datetime** | When an Owner/Admin turned on the requirement that every member of this organization protects their account with a second factor; null means it is optional. A reversible policy toggle, stamped like {@see User::$disabledAt} rather than a verdict, so no \&quot;who set it\&quot; attribution. | [optional] [readonly] 
**api_access_log_retention_days** | **int** | How long this organization&#39;s {@see \\App\\Entity\\ApiAccessLogEntry} rows are kept before {@see \\App\\MessageHandler\\PurgeApiAccessLogHandler} prunes them. Null means \&quot;the platform default\&quot; ({@see \\App\\Service\\ApiAccessLogRetention::DEFAULT_DAYS}) rather than a fixed number baked into every organization row the day this shipped. | [optional] [readonly] 
**memberships** | [**List[Membership]**](Membership.md) |  | [optional] [readonly] 
**applications** | **List[str]** |  | [optional] [readonly] 
**swarms** | **List[str]** | BYO swarms owned by this organization. | [optional] [readonly] 
**machines** | [**List[Machine]**](Machine.md) | Machines self-service-provisioned for this organization. | [optional] [readonly] 
**credit_transactions** | **List[str]** | The append-only credit ledger. | [optional] [readonly] 
**signals** | [**List[OrganizationSignal]**](OrganizationSignal.md) | What this organization&#39;s own compose files have told the platform about it (#818). | [optional] [readonly] 
**id** | **UUID** |  | [optional] [readonly] 
**deleted_at** | **datetime** |  | [optional] [readonly] 
**created_at** | **datetime** |  | [optional] [readonly] 
**updated_at** | **datetime** |  | [optional] [readonly] 
**tier_pinned** | **bool** |  | [optional] [readonly] 
**deleted** | **bool** |  | [optional] [readonly] 

## Example

```python
from someones_computer_sdk.models.organization import Organization

# TODO update the JSON string below
json = "{}"
# create an instance of Organization from a JSON string
organization_instance = Organization.from_json(json)
# print the JSON string representation of the object
print(Organization.to_json())

# convert the object into a dict
organization_dict = organization_instance.to_dict()
# create an instance of Organization from a dict
organization_from_dict = Organization.from_dict(organization_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


