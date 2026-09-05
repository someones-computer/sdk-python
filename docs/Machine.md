# Machine


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**instance** | [**ProxmoxInstance**](ProxmoxInstance.md) |  | [optional] 
**node** | **str** | The node within the instance — same string &#x60;app:proxmox:template&#x60; builds on. | [optional] 
**vmid** | **int** |  | [optional] 
**name** | **str** | How an operator addresses it; also the guest hostname the seed sets. | [optional] 
**size** | **str** |  | [optional] 
**disk_blocks** | **int** | Disk as a block count, never gigabytes: a thin volume grows and never shrinks, so the invariant worth enforcing is \&quot;this number only goes up\&quot;, and a count makes that checkable where a free-form size would not. | [optional] [readonly] [default to 1]
**template_vmid** | **int** | The template this was cloned from, by vmid. The reference count that decides when a superseded template may be deleted (§03): linked clones pin their base disk, and Proxmox will refuse — rightly — to delete a template that still has children. | [optional] 
**address** | **str** | The island address chosen by the control plane&#39;s pool and registered with Proxmox, which is what dnsmasq then answers the machine&#39;s DHCP request with (docs/island-network.md — Proxmox&#39;s IPAM cannot allocate, so the platform still picks). Null until allocation; unique so the pool cannot double-allocate even if two provisions race. | [optional] 
**state** | **str** |  | [optional] [default to 'requested']
**failure** | **str** | Why &#x60;Failed&#x60;, when it is. Carries the task&#39;s own words, never a paraphrase. | [optional] [readonly] 
**provision_attempt** | **int** | Which run through the flow this is, starting at 1 and incremented on every {@see self::reprovision()}. {@see \\App\\Entity\\ProvisioningLogLine} tags each captured line with the value that was current when it was written, so a retry&#39;s transcript starts fresh rather than appending to the failed attempt before it. | [optional] [readonly] [default to 1]
**provision_started_at** | **datetime** | When the current run through the flow began — set at construction and reset on every {@see self::reprovision()}, mirroring {@see ProxmoxInstance::$templateBuildStartedAt}. What {@see self::isProvisioningStale()} measures against: the real ceiling is the flow&#39;s own step deadlines ({@see \\App\\MessageHandler\\ProvisionMachineHandler}&#39;s &#x60;BOOT_DEADLINE&#x60;/&#x60;TASK_DEADLINE&#x60;), and a run still going past {@see self::PROVISION_PRESUMED_DEAD_AFTER} is a worker that died holding it — a crash, an OOM, a deploy restart — rather than one still working. | [optional] [readonly] 
**swarm** | **str** | The context this machine serves, if any. Nullable on purpose — see the class docblock. | [optional] 
**organization** | **str** | The organization this machine was self-service-provisioned for, or null for one an operator made through &#x60;/admin/machines&#x60;. Nullable for the same reason &#x60;$swarm&#x60; is: an admin-made machine belongs to nobody&#39;s tenancy, and this column must not invent an owner for it. Set once, at creation, to the same organization that owns the paired &#x60;$swarm&#x60; — {@see Organization::markDeleted()} detaches it rather than deleting the row, matching how a BYO context&#39;s owner is handled. | [optional] 
**id** | **str** |  | [optional] [readonly] 
**created_at** | **datetime** |  | [optional] [readonly] 
**updated_at** | **datetime** |  | [optional] [readonly] 
**disk_gigabytes** | **int** |  | [optional] [readonly] 
**provisioning_stale** | **bool** | Still mid-flow, and has been for longer than any healthy run takes — what {@see \\App\\MessageHandler\\SweepStaleMachineProvisionsHandler} sweeps for. A worker that crashed, OOM&#39;d, or was recycled mid-step leaves the row exactly where it stood; nothing else ever revisits it, since the handler&#39;s own guard is \&quot;state is Requested\&quot; and every other step only ever moves the flow forward. | [optional] [readonly] 

## Example

```python
from someones_computer_sdk.models.machine import Machine

# TODO update the JSON string below
json = "{}"
# create an instance of Machine from a JSON string
machine_instance = Machine.from_json(json)
# print the JSON string representation of the object
print(Machine.to_json())

# convert the object into a dict
machine_dict = machine_instance.to_dict()
# create an instance of Machine from a dict
machine_from_dict = Machine.from_dict(machine_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


