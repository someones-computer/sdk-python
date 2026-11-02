# Volume

List the volumes the caller can see.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**organization** | **str** |  | [optional] 
**slug** | **str** |  | [optional] 
**id** | **UUID** |  | [optional] [readonly] 
**deleted_at** | **datetime** |  | [optional] [readonly] 
**created_at** | **datetime** |  | [optional] [readonly] 
**updated_at** | **datetime** |  | [optional] [readonly] 
**state** | **str** | The bucket&#39;s state, as the volume&#39;s own. | [optional] [readonly] 
**usage_bytes** | **int** | Bytes the bucket holds at the last measurement, or null before the first. | [optional] [readonly] 
**deleted** | **bool** |  | [optional] [readonly] 

## Example

```python
from someones_computer_sdk.models.volume import Volume

# TODO update the JSON string below
json = "{}"
# create an instance of Volume from a JSON string
volume_instance = Volume.from_json(json)
# print the JSON string representation of the object
print(Volume.to_json())

# convert the object into a dict
volume_dict = volume_instance.to_dict()
# create an instance of Volume from a dict
volume_from_dict = Volume.from_dict(volume_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


