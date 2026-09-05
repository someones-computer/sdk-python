# ServiceMemReservation

Memory floor in bytes (`deploy.resources.reservations.memory`), null = nothing declared.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------

## Example

```python
from someones_computer_sdk.models.service_mem_reservation import ServiceMemReservation

# TODO update the JSON string below
json = "{}"
# create an instance of ServiceMemReservation from a JSON string
service_mem_reservation_instance = ServiceMemReservation.from_json(json)
# print the JSON string representation of the object
print(ServiceMemReservation.to_json())

# convert the object into a dict
service_mem_reservation_dict = service_mem_reservation_instance.to_dict()
# create an instance of ServiceMemReservation from a dict
service_mem_reservation_from_dict = ServiceMemReservation.from_dict(service_mem_reservation_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


