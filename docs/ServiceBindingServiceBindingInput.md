# ServiceBindingServiceBindingInput

That an application may use a managed service — the join the per-application toggle could not express.  Many-to-many by construction: one database can back a web app and its worker, and one application can hold several bindings. Unbinding leaves the data alone; only destroying the {@see ManagedService} touches it.  A binding is also where the *deployment* seam lives. It records which variable names it injects, so the UI can say what an application will receive before it receives it, and so the resolver can show an operator-set variable shadowing a binding rather than silently losing to it.  **Creating one is a permission, not a provisioning step** — nothing at the engine moves. Deleting one withdraws that permission and touches no data, which is why `DELETE` here is a hard delete and `DELETE` on a {@see ManagedService} is not the same kind of verb at all.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**application** | **str** |  | 
**service** | **str** |  | 

## Example

```python
from someones_computer_sdk.models.service_binding_service_binding_input import ServiceBindingServiceBindingInput

# TODO update the JSON string below
json = "{}"
# create an instance of ServiceBindingServiceBindingInput from a JSON string
service_binding_service_binding_input_instance = ServiceBindingServiceBindingInput.from_json(json)
# print the JSON string representation of the object
print(ServiceBindingServiceBindingInput.to_json())

# convert the object into a dict
service_binding_service_binding_input_dict = service_binding_service_binding_input_instance.to_dict()
# create an instance of ServiceBindingServiceBindingInput from a dict
service_binding_service_binding_input_from_dict = ServiceBindingServiceBindingInput.from_dict(service_binding_service_binding_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


