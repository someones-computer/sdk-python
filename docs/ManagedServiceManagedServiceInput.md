# ManagedServiceManagedServiceInput

Create a new managed service (database or bucket) on a shared engine.

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


