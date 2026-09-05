# SwarmJsonMergePatch

A Docker Swarm we can deploy onto. The trust boundary of the platform.  owner === null  => PLATFORM pool (shared infra we run). owner !== null  => CUSTOMER BYO cluster (untrusted, outbound-only).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**owner** | **str** | Null for the platform pool; set for a customer BYO cluster. | [optional] 
**kind** | **str** |  | [optional] [readonly] 
**name** | **str** |  | [optional] 
**endpoint** | **str** | Manager API endpoint (tcp+TLS) or SSH target. | [optional] 
**status** | **str** |  | [optional] [default to 'unreachable']
**public_host** | **str** | The address a client *outside* the cluster reaches this context&#39;s published ports on — a hostname or an IP, no scheme and no port. | [optional] 
**roles** | **List[str]** | What this context is used for — builds, runtime, or both. Stored as the enum&#39;s string values rather than a relation: it is a small fixed set, and a json column needs no join to answer \&quot;where can I build?\&quot;. | [optional] [default to [runtime]]
**last_seen_at** | **datetime** |  | [optional] 
**capacity** | **Dict[str, Optional[str]]** | Observed capacity snapshot (cpu/mem/nodes), reconciled from the swarm — whatever {@see \\App\\Service\\Swarm\\SwarmHealth::$capacity} carried at the last successful probe. | [optional] 
**labels** | **Dict[str, str]** |  | [optional] [readonly] 
**ingress_installed_at** | **datetime** | When {@see \\App\\Service\\Ingress\\TraefikInstaller} last stood up (or confirmed) the edge on this context, dispatched automatically once it becomes a platform-owned runtime context. | [optional] [readonly] 
**ingress_error** | **str** | What the last automatic install attempt said, when it failed. Cleared on a success so the row never shows a stale complaint next to a working edge. | [optional] [readonly] 
**ingress_network** | **str** | The shared overlay that install put the edge on — the one Traefik&#39;s &#x60;--providers.swarm.network&#x60; names, and therefore the only network a service can be routed from. | [optional] [readonly] 
**ingress_verified_at** | **datetime** | When the edge was last *observed* routing — the overlay present, the edge service on it, watching it, with a task running ({@see \\App\\Service\\Ingress\\IngressVerifier}). | [optional] [readonly] 
**ingress_verification_error** | **str** | What the last verification found wrong, or null when the edge was routing. | [optional] [readonly] 
**nodes** | [**List[SwarmNode]**](SwarmNode.md) |  | [optional] 
**machines** | [**List[Machine]**](Machine.md) |  | [optional] 
**deployments** | **List[str]** | The revisions placed here. Mapped for the same single reason as {@see self::$machines} — so a delete can let go of them — rather than as a collection anything reads; {@see \\App\\Repository\\DeploymentRepository} is where a caller asks what is on a context. | [optional] 
**id** | **str** |  | [optional] [readonly] 
**deleted_at** | **datetime** |  | [optional] [readonly] 
**created_at** | **datetime** |  | [optional] [readonly] 
**updated_at** | **datetime** |  | [optional] [readonly] 
**platform_owned** | **bool** |  | [optional] [readonly] 
**platform_provisioned** | **bool** | Whether the platform itself stood this context up, whoever currently owns the row — a machine {@see \\App\\MessageHandler\\ProvisionMachineHandler} provisioned, running this platform&#39;s own trusted image, versus a customer&#39;s own cluster registered straight through {@see \\App\\Controller\\Admin\\SwarmController}. | [optional] [readonly] 
**working_edge** | **bool** | Whether a revision that publishes a port can be routed here. | [optional] [readonly] 
**deleted** | **bool** |  | [optional] [readonly] 

## Example

```python
from someones_computer_sdk.models.swarm_json_merge_patch import SwarmJsonMergePatch

# TODO update the JSON string below
json = "{}"
# create an instance of SwarmJsonMergePatch from a JSON string
swarm_json_merge_patch_instance = SwarmJsonMergePatch.from_json(json)
# print the JSON string representation of the object
print(SwarmJsonMergePatch.to_json())

# convert the object into a dict
swarm_json_merge_patch_dict = swarm_json_merge_patch_instance.to_dict()
# create an instance of SwarmJsonMergePatch from a dict
swarm_json_merge_patch_from_dict = SwarmJsonMergePatch.from_dict(swarm_json_merge_patch_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


