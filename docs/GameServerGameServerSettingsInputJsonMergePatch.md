# GameServerGameServerSettingsInputJsonMergePatch

Replace the settings, and optionally the version, of a game server. A running server restarts to apply them.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**settings** | **Dict[str, Optional[str]]** |  | [optional] 
**version** | **str** |  | [optional] 

## Example

```python
from someones_computer_sdk.models.game_server_game_server_settings_input_json_merge_patch import GameServerGameServerSettingsInputJsonMergePatch

# TODO update the JSON string below
json = "{}"
# create an instance of GameServerGameServerSettingsInputJsonMergePatch from a JSON string
game_server_game_server_settings_input_json_merge_patch_instance = GameServerGameServerSettingsInputJsonMergePatch.from_json(json)
# print the JSON string representation of the object
print(GameServerGameServerSettingsInputJsonMergePatch.to_json())

# convert the object into a dict
game_server_game_server_settings_input_json_merge_patch_dict = game_server_game_server_settings_input_json_merge_patch_instance.to_dict()
# create an instance of GameServerGameServerSettingsInputJsonMergePatch from a dict
game_server_game_server_settings_input_json_merge_patch_from_dict = GameServerGameServerSettingsInputJsonMergePatch.from_dict(game_server_game_server_settings_input_json_merge_patch_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


