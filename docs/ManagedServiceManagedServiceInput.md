# ManagedServiceManagedServiceInput

One tenant's database or bucket on a shared engine.  **Owned by an organization and bound to applications** — not a per-application toggle. The distinction is the whole reason this entity exists in this shape: a toggle with a unique foreign key cannot express one database backing both a web app and its worker, and cannot survive an application being rebuilt under a new name. Binding is therefore explicit ({@see ServiceBinding}), which costs one step at creation and buys sharing, one billing shape, one permission model and one set of verbs across databases *and* buckets.  A bucket is the same noun with a different {@see $kind}. Only the driver that executes the tenancy operations differs.  Soft-deleted, so a destroy is recoverable within its grace period ({@see ManagedServiceRepository::GRACE_PERIOD}); only the driver's `DROP` is not, and that runs on the far side of it.  **Read is scoped by membership and writing by role**, which are different questions: {@see \\App\\ApiResource\\ManagedServiceOwnerExtension} filters the query, so another tenant's id answers 404 rather than confirming it exists, while {@see \\App\\Security\\Voter\\ManageVoter} governs the verbs inside each processor — a plain member may see their organization's databases without being able to destroy one.  Delete does *not* fall through to the generic soft-delete processor: dropping a database is not stamping a column, and the difference is a tenant's data. See {@see \\App\\State\\ManagedServiceDestroyProcessor}.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**engine** | **str** | The engine, as the catalogue names it — &#x60;postgres:17&#x60;, &#x60;mysql:8.0&#x60;. | [default to '']
**slug** | **str** | The tenant&#39;s own name for it — what appears in the UI and in &#x60;sc service ls&#x60;. | [default to '']
**organization** | **str** |  | 

## Example

```python
from someones_computer_sdk.models.managed_service_managed_service_input import ManagedServiceManagedServiceInput

# TODO update the JSON string below
json = "{}"
# create an instance of ManagedServiceManagedServiceInput from a JSON string
managed_service_managed_service_input_instance = ManagedServiceManagedServiceInput.from_json(json)
# print the JSON string representation of the object
print(ManagedServiceManagedServiceInput.to_json())

# convert the object into a dict
managed_service_managed_service_input_dict = managed_service_managed_service_input_instance.to_dict()
# create an instance of ManagedServiceManagedServiceInput from a dict
managed_service_managed_service_input_from_dict = ManagedServiceManagedServiceInput.from_dict(managed_service_managed_service_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


