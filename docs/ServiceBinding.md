# ServiceBinding

That an application may use a managed service — the join the per-application toggle could not express.  Many-to-many by construction: one database can back a web app and its worker, and one application can hold several bindings. Unbinding leaves the data alone; only destroying the {@see ManagedService} touches it.  A binding is also where the *deployment* seam lives. It records which variable names it injects, so the UI can say what an application will receive before it receives it, and so the resolver can show an operator-set variable shadowing a binding rather than silently losing to it.  **Creating one is a permission, not a provisioning step** — nothing at the engine moves. Deleting one withdraws that permission and touches no data, which is why `DELETE` here is a hard delete and `DELETE` on a {@see ManagedService} is not the same kind of verb at all.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**application** | **str** |  | [optional] 
**service** | **str** |  | [optional] 
**injected_keys** | **List[str]** | The environment variable names this binding contributes — one &#x60;DATABASE_URL&#x60; for a database, the four &#x60;S3_*&#x60; names for a bucket. | [optional] 
**sidecar_service_name** | **str** | What the sidecar is called inside the tenant&#39;s stack — &#x60;db&#x60; unless something else claimed the name first. | [optional] [default to 'db']
**adopted_compose_service** | **str** | The compose service this binding replaced, or null for a binding somebody asked for directly. | [optional] 
**id** | **str** |  | [optional] [readonly] 
**created_at** | **datetime** |  | [optional] [readonly] 
**updated_at** | **datetime** |  | [optional] [readonly] 
**adopted** | **bool** |  | [optional] [readonly] 
**sidecar_credential** | [**SealedSecret**](SealedSecret.md) |  | [optional] 

## Example

```python
from someones_computer_sdk.models.service_binding import ServiceBinding

# TODO update the JSON string below
json = "{}"
# create an instance of ServiceBinding from a JSON string
service_binding_instance = ServiceBinding.from_json(json)
# print the JSON string representation of the object
print(ServiceBinding.to_json())

# convert the object into a dict
service_binding_dict = service_binding_instance.to_dict()
# create an instance of ServiceBinding from a dict
service_binding_from_dict = ServiceBinding.from_dict(service_binding_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


