# GameServerGameServerInput

Create a game server, stopped. Start it next. An unset version takes the default, and an unset volume makes a new one.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**organization** | **str** |  | 
**slug** | **str** |  | [default to '']
**name** | **str** |  | [default to '']
**kind** | **str** |  | 
**version** | **str** | Null takes the game&#39;s default version. | [optional] 
**settings** | **Dict[str, Optional[str]]** | The fields of the game&#39;s settings schema. A field left out takes its default. | [optional] 
**volume** | **str** | The slug of an unused volume in the organization. Null makes a new volume named like the server. | [optional] 

## Example

```python
from someones_computer_sdk.models.game_server_game_server_input import GameServerGameServerInput

# TODO update the JSON string below
json = "{}"
# create an instance of GameServerGameServerInput from a JSON string
game_server_game_server_input_instance = GameServerGameServerInput.from_json(json)
# print the JSON string representation of the object
print(GameServerGameServerInput.to_json())

# convert the object into a dict
game_server_game_server_input_dict = game_server_game_server_input_instance.to_dict()
# create an instance of GameServerGameServerInput from a dict
game_server_game_server_input_from_dict = GameServerGameServerInput.from_dict(game_server_game_server_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


