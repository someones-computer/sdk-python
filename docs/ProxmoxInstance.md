# ProxmoxInstance


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**endpoint** | **str** | Base URL of the API, scheme and authority only — &#x60;https://10.0.0.68:8006&#x60;. | [optional] 
**token_id** | **str** | Full token identifier, &#x60;user@realm!tokenid&#x60; — e.g. &#x60;root@pam!someones-computer&#x60;. | [optional] 
**token_secret** | **str** | The token&#39;s secret (a UUID as Proxmox issues it), encrypted at rest and never serialized. Proxmox shows it exactly once, at creation. | [optional] 
**verify_tls** | **bool** | Whether the certificate must validate against a CA chain. | [optional] [default to True]
**public_key_pin** | **str** | base64 SHA-256 of the endpoint&#39;s SubjectPublicKeyInfo — curl&#39;s &#x60;pin-sha256&#x60;. The right answer for a self-signed Proxmox: it authenticates *this specific host* without any CA, so the connection is still protected against interception, which &#x60;verifyTls &#x3D; false&#x60; alone is not. | [optional] 
**status** | **str** |  | [optional] [default to 'unreachable']
**last_seen_at** | **datetime** |  | [optional] 
**last_error** | **str** | Why the last probe failed, kept so an operator can tell a revoked token from a dead host without re-running anything. Cleared on success. | [optional] 
**version** | **Dict[str, Optional[str]]** | Observed &#x60;GET /version&#x60; snapshot (release, repoid). Observed state, so it is whatever the last probe saw and is never authoritative. | [optional] 
**template_vmid** | **int** | The vmid of the Alpine template &#x60;app:proxmox:template&#x60; last built here, or null if it has never been run against this endpoint. This is what makes a template&#39;s existence something the app can answer without an SSH session and a &#x60;qm list&#x60; — the gap that sent an operator to do exactly that. | [optional] [readonly] 
**template_alpine_version** | **str** | The Alpine version baked into {@see $templateVmid}, e.g. &#x60;3.23.0&#x60;. | [optional] [readonly] 
**template_built_at** | **datetime** |  | [optional] [readonly] 
**template_build_started_at** | **datetime** | When a background template build was dispatched for this endpoint, or null when none is in flight — the only trace a build leaves while it runs. | [optional] [readonly] 
**template_build_failures** | **int** | How many builds in a row have failed since the last success, incremented by {@see \\App\\MessageHandler\\BuildProxmoxTemplateHandler}&#39;s catch block and cleared by {@see recordTemplateBuilt()}. This is what {@see templateBuildIsBackedOff()} backs the retry off against — without it, {@see \\App\\MessageHandler\\CheckProxmoxTemplatesHandler} redispatches a build every tick regardless of how many times it has already failed (#1059). | [optional] [readonly] [default to 0]
**id** | **str** |  | [optional] [readonly] 
**created_at** | **datetime** |  | [optional] [readonly] 
**updated_at** | **datetime** |  | [optional] [readonly] 
**template** | **bool** | Whether &#x60;app:proxmox:template&#x60; has ever recorded a build against this endpoint. | [optional] [readonly] 

## Example

```python
from someones_computer_sdk.models.proxmox_instance import ProxmoxInstance

# TODO update the JSON string below
json = "{}"
# create an instance of ProxmoxInstance from a JSON string
proxmox_instance_instance = ProxmoxInstance.from_json(json)
# print the JSON string representation of the object
print(ProxmoxInstance.to_json())

# convert the object into a dict
proxmox_instance_dict = proxmox_instance_instance.to_dict()
# create an instance of ProxmoxInstance from a dict
proxmox_instance_from_dict = ProxmoxInstance.from_dict(proxmox_instance_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


