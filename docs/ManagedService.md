# ManagedService

One tenant's database or bucket on a shared engine.  **Owned by an organization and bound to applications** — not a per-application toggle. The distinction is the whole reason this entity exists in this shape: a toggle with a unique foreign key cannot express one database backing both a web app and its worker, and cannot survive an application being rebuilt under a new name. Binding is therefore explicit ({@see ServiceBinding}), which costs one step at creation and buys sharing, one billing shape, one permission model and one set of verbs across databases *and* buckets.  A bucket is the same noun with a different {@see $kind}. Only the driver that executes the tenancy operations differs.  Soft-deleted, so a destroy is recoverable within its grace period ({@see ManagedServiceRepository::GRACE_PERIOD}); only the driver's `DROP` is not, and that runs on the far side of it.  **Read is scoped by membership and writing by role**, which are different questions: {@see \\App\\ApiResource\\ManagedServiceOwnerExtension} filters the query, so another tenant's id answers 404 rather than confirming it exists, while {@see \\App\\Security\\Voter\\ManageVoter} governs the verbs inside each processor — a plain member may see their organization's databases without being able to destroy one.  Delete does *not* fall through to the generic soft-delete processor: dropping a database is not stamping a column, and the difference is a tenant's data. See {@see \\App\\State\\ManagedServiceDestroyProcessor}.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**organization** | **str** |  | [optional] 
**slug** | **str** |  | [optional] 
**kind** | **str** | The catalogue entry the tenant picked, as &#x60;(kind, majorVersion)&#x60;. | [optional] 
**major_version** | **str** |  | [optional] 
**instance** | [**ServiceInstance**](ServiceInstance.md) |  | [optional] 
**backing_name** | **str** | What the object is actually called inside the engine — &#x60;acme_hearth_db&#x60; for a database, &#x60;acme-hearth-media&#x60; for a bucket. | [optional] 
**external_key_id** | **str** | A bucket&#39;s access key id — the non-secret half of a Garage key, paired with {@see $credentialCiphertext}&#39;s sealed secret access key. Null for every database kind, which has no such pair: its one credential is a password, sealed whole into the four columns above. | [optional] 
**quota_bytes** | [**ManagedServiceQuotaBytes**](ManagedServiceQuotaBytes.md) |  | [optional] 
**pool_size_override** | **int** | Operator override of the backend pool size — how many connections each of this service&#39;s proxies holds open to the engine (&#x60;default_pool_size&#x60; on pgbouncer, &#x60;mysql_servers.max_connections&#x60; on ProxySQL). Null means the generator&#39;s own default; the effective number is always asked of the generator ({@see \\App\\Service\\ManagedService\\Sidecar\\SidecarConfigGenerator::poolSizeFor()}), never read from here directly, so the default lives in one place. | [optional] 
**client_connections_override** | **int** | Operator override of the client-side connection ceiling — how many client connections each proxy will accept (&#x60;max_client_conn&#x60; on pgbouncer, &#x60;mysql-max_connections&#x60; on ProxySQL). Same null-means-default and ask-the-generator contract as {@see $poolSizeOverride}. | [optional] 
**state** | **str** |  | [optional] [default to 'requested']
**failure_reason** | **str** |  | [optional] [readonly] 
**suspension_reason** | **str** | Why the service is suspended, or null when a state of &#x60;suspended&#x60; was put there by an operator or the tenant rather than by the platform. | [optional] 
**usage_bytes** | [**ManagedServiceUsageBytes**](ManagedServiceUsageBytes.md) |  | [optional] 
**usage_sampled_at** | **datetime** |  | [optional] [readonly] 
**last_load_millis** | [**ManagedServiceLastLoadMillis**](ManagedServiceLastLoadMillis.md) |  | [optional] 
**last_load_sampled_at** | **datetime** |  | [optional] [readonly] 
**pending_load_millis** | [**ManagedServicePendingLoadMillis**](ManagedServicePendingLoadMillis.md) |  | [optional] 
**bindings** | **List[str]** |  | [optional] 
**id** | **str** |  | [optional] [readonly] 
**deleted_at** | **datetime** |  | [optional] [readonly] 
**created_at** | **datetime** |  | [optional] [readonly] 
**updated_at** | **datetime** |  | [optional] [readonly] 
**catalogue_entry** | **str** | &#x60;postgres 17&#x60;, &#x60;mysql 8.0&#x60; — the catalogue entry, as one string. | [optional] [readonly] 
**credential** | [**SealedSecret**](SealedSecret.md) |  | [optional] 
**available** | **bool** |  | [optional] [readonly] 
**deleted** | **bool** |  | [optional] [readonly] 

## Example

```python
from someones_computer_sdk.models.managed_service import ManagedService

# TODO update the JSON string below
json = "{}"
# create an instance of ManagedService from a JSON string
managed_service_instance = ManagedService.from_json(json)
# print the JSON string representation of the object
print(ManagedService.to_json())

# convert the object into a dict
managed_service_dict = managed_service_instance.to_dict()
# create an instance of ManagedService from a dict
managed_service_from_dict = ManagedService.from_dict(managed_service_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


