# ServiceCpuReservation

Nanoseconds of CPU the scheduler should hold for each replica (compose `deploy.resources.reservations.cpus`), null = nothing declared.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------

## Example

```python
from someones_computer_sdk.models.service_cpu_reservation import ServiceCpuReservation

# TODO update the JSON string below
json = "{}"
# create an instance of ServiceCpuReservation from a JSON string
service_cpu_reservation_instance = ServiceCpuReservation.from_json(json)
# print the JSON string representation of the object
print(ServiceCpuReservation.to_json())

# convert the object into a dict
service_cpu_reservation_dict = service_cpu_reservation_instance.to_dict()
# create an instance of ServiceCpuReservation from a dict
service_cpu_reservation_from_dict = ServiceCpuReservation.from_dict(service_cpu_reservation_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


