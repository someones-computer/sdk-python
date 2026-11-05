# GameServerGameServerRead

List the game servers the caller can see. A server that is starting or stopping is brought up to date first.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**organization** | **str** |  | [optional] 
**slug** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**kind** | **str** |  | [optional] 
**version** | **str** |  | [optional] 
**settings** | [**Dict[str, GameServerGameServerReadSettingsValue]**](GameServerGameServerReadSettingsValue.md) |  | [optional] 
**state** | **str** | The reason only means something for &#x60;failed&#x60;, so any other state clears it. | [optional] [default to 'stopped']
**state_reason** | **str** | Why the server is &#x60;failed&#x60;, in words a tenant can read. Null in every other state. | [optional] [readonly] 
**volume** | **str** | The volume&#39;s slug, so a client can name the world without the bucket behind it. | [optional] [readonly] 

## Example

```python
from someones_computer_sdk.models.game_server_game_server_read import GameServerGameServerRead

# TODO update the JSON string below
json = "{}"
# create an instance of GameServerGameServerRead from a JSON string
game_server_game_server_read_instance = GameServerGameServerRead.from_json(json)
# print the JSON string representation of the object
print(GameServerGameServerRead.to_json())

# convert the object into a dict
game_server_game_server_read_dict = game_server_game_server_read_instance.to_dict()
# create an instance of GameServerGameServerRead from a dict
game_server_game_server_read_from_dict = GameServerGameServerRead.from_dict(game_server_game_server_read_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


