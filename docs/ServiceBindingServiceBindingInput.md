# ServiceBindingServiceBindingInput

Bind a managed service to an application.

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


