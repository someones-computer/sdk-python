# ManagedServiceEngine


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | The engine&#39;s handle, such as &#x60;pg17-1&#x60;. | [optional] 
**state** | **str** | The state of the engine, such as &#x60;serving&#x60; or &#x60;failed&#x60;. | [optional] 

## Example

```python
from someones_computer_sdk.models.managed_service_engine import ManagedServiceEngine

# TODO update the JSON string below
json = "{}"
# create an instance of ManagedServiceEngine from a JSON string
managed_service_engine_instance = ManagedServiceEngine.from_json(json)
# print the JSON string representation of the object
print(ManagedServiceEngine.to_json())

# convert the object into a dict
managed_service_engine_dict = managed_service_engine_instance.to_dict()
# create an instance of ManagedServiceEngine from a dict
managed_service_engine_from_dict = ManagedServiceEngine.from_dict(managed_service_engine_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


