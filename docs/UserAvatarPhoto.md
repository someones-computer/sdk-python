# UserAvatarPhoto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**photo** | **str** | Base64 of the raw image bytes — see {@see User::getAvatarPhoto()} for why text rather than a BLOB. | [optional] [readonly] 
**type** | **str** | The media type sniffed from the bytes ({@see \\App\\Service\\DirectoryPhoto}), nullable like the old &#x60;avatar_photo_type&#x60; column was: bytes can be stored without a type, and {@see \\App\\Controller\\AvatarController} falls back to &#x60;application/octet-stream&#x60;. | [optional] 
**id** | **str** |  | [optional] [readonly] 

## Example

```python
from someones_computer_sdk.models.user_avatar_photo import UserAvatarPhoto

# TODO update the JSON string below
json = "{}"
# create an instance of UserAvatarPhoto from a JSON string
user_avatar_photo_instance = UserAvatarPhoto.from_json(json)
# print the JSON string representation of the object
print(UserAvatarPhoto.to_json())

# convert the object into a dict
user_avatar_photo_dict = user_avatar_photo_instance.to_dict()
# create an instance of UserAvatarPhoto from a dict
user_avatar_photo_from_dict = UserAvatarPhoto.from_dict(user_avatar_photo_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


