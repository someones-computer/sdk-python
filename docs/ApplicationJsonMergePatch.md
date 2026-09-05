# ApplicationJsonMergePatch

A deployable \"island\": one logical app, defined by a compose file, deployed as a swarm stack. Holds a pointer to the current (immutable) deployment; history lives in the deployment revisions.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**organization** | **str** | Re-home this application. Callers own everything the uniqueness constraint and the trust invariant elsewhere in the platform expect of a move — the entity itself only holds the pointer. | [optional] 
**slug** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**isolation_level** | **str** |  | [optional] [default to 'shared']
**service_adoption** | **str** | Whether a deploy&#39;s compose file is watched for services a managed equivalent could replace. | [optional] [default to 'off']
**access_gate** | **str** | How this application&#39;s routed HTTP services are gated at the edge — &#x60;None&#x60; by default, so an application behaves exactly as it always has until an org manager opts it in ({@see AccessGateMode}). | [optional] [default to 'none']
**current_deployment** | **str** | Pointer to the currently active revision; null before the first deploy. | [optional] 
**first_running_at** | **datetime** | The first moment any revision of this application ever reached &#x60;running&#x60; — null until it has. What {@see \\App\\Service\\Teardown\\TeardownGracePeriod} measures grace-period uptime from, in place of the current revision&#39;s own &#x60;createdAt&#x60; (#1307): a revision row is stamped at bundle ingest and a fresh one is created on every &#x60;sc deploy&#x60;, so measuring off it gave a six-month-old production application a ten-minute grace period the moment it was redeployed. This is set once and never moved — a redeploy, or reactivating an old revision, does not reset it, because the application&#39;s history is what earns the longer grace, not whichever revision happens to be current. | [optional] [readonly] 
**primary_deployment_name** | **str** | Which deployment *name* owns the application&#39;s apex identity — the stack, network and hostname that carry no revision component ({@see \\App\\Service\\Placement\\StackNaming}). | [optional] 
**legacy_stack_base** | **str** | The &#x60;&lt;prefix&gt;-&lt;org&gt;-&lt;app&gt;&#x60; join this application&#39;s stacks were **already named from**, before the separator was made unambiguous — or null, meaning nothing of this application has ever been on a swarm under the old name and {@see \\App\\Service\\Placement\\StackNaming} is free to derive the current one. | [optional] 
**icon_key** | **str** | Object key of this application&#39;s stored icon, or null when nobody has given it one — in which case {@see \\App\\Service\\Icon\\GeneratedIcon} draws one from the name and slug, so every application has an icon either way. | [optional] [readonly] 
**icon_source** | **str** | Where {@see $iconKey} came from — null exactly when there is no stored icon. | [optional] [readonly] 
**build_bucket** | **str** | This application&#39;s own Garage build-context bucket — where &#x60;sc deploy&#x60;&#39;s uploaded contexts and forwarded images are parked, and the only bucket the build key below can read. Null until the first upload provisions it ({@see \\App\\Service\\Bundle\\ApplicationBuildBucketProvisioner}); every application predating #996 looks like that too, and provisions on its next deploy. | [optional] 
**build_key_id** | **str** | The access-key id of the read-only Garage key scoped to {@see $buildBucket}, handed to build tasks. Doubles as Garage&#39;s own identifier for the key (the same way {@see ManagedService::$externalKeyId} does), so nothing separate is persisted for it. | [optional] 
**deployments** | **List[str]** |  | [optional] 
**variables** | [**List[Variable]**](Variable.md) |  | [optional] 
**port_allocations** | [**List[PortAllocation]**](PortAllocation.md) |  | [optional] 
**id** | **str** |  | [optional] [readonly] 
**deleted_at** | **datetime** |  | [optional] [readonly] 
**created_at** | **datetime** |  | [optional] [readonly] 
**updated_at** | **datetime** |  | [optional] [readonly] 
**build_credential** | [**SealedSecret**](SealedSecret.md) |  | [optional] 
**access_gate_credential** | [**SealedSecret**](SealedSecret.md) |  | [optional] 
**icon** | **str** | Point the application at a stored icon, or at none. | [optional] 
**operator_chosen_icon** | **bool** | Whether the stored icon was chosen by a person, and so must survive the next deploy&#39;s favicon extraction. | [optional] [readonly] 
**icon_version** | **str** | A short, stable token for the icon a caller is looking at — the cache-busting half of the icon URL, and null when there is nothing stored to bust. | [optional] [readonly] 
**deleted** | **bool** |  | [optional] [readonly] 

## Example

```python
from someones_computer_sdk.models.application_json_merge_patch import ApplicationJsonMergePatch

# TODO update the JSON string below
json = "{}"
# create an instance of ApplicationJsonMergePatch from a JSON string
application_json_merge_patch_instance = ApplicationJsonMergePatch.from_json(json)
# print the JSON string representation of the object
print(ApplicationJsonMergePatch.to_json())

# convert the object into a dict
application_json_merge_patch_dict = application_json_merge_patch_instance.to_dict()
# create an instance of ApplicationJsonMergePatch from a dict
application_json_merge_patch_from_dict = ApplicationJsonMergePatch.from_dict(application_json_merge_patch_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


