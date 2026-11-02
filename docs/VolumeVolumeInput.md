# VolumeVolumeInput

Create a volume: a named store for a game server, held in a Garage bucket.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**slug** | **str** | The tenant&#39;s own name for it. It shows in the panel and in a game server&#39;s settings. | [default to '']
**organization** | **str** |  | 

## Example

```python
from someones_computer_sdk.models.volume_volume_input import VolumeVolumeInput

# TODO update the JSON string below
json = "{}"
# create an instance of VolumeVolumeInput from a JSON string
volume_volume_input_instance = VolumeVolumeInput.from_json(json)
# print the JSON string representation of the object
print(VolumeVolumeInput.to_json())

# convert the object into a dict
volume_volume_input_dict = volume_volume_input_instance.to_dict()
# create an instance of VolumeVolumeInput from a dict
volume_volume_input_from_dict = VolumeVolumeInput.from_dict(volume_volume_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


