# someones_computer_sdk.GameServerApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**game_servers_create**](GameServerApi.md#game_servers_create) | **POST** /api/game_servers | Creates a GameServer resource.
[**game_servers_delete**](GameServerApi.md#game_servers_delete) | **DELETE** /api/game_servers/{id} | Removes the GameServer resource.
[**game_servers_get**](GameServerApi.md#game_servers_get) | **GET** /api/game_servers/{id} | Retrieves a GameServer resource.
[**game_servers_list**](GameServerApi.md#game_servers_list) | **GET** /api/game_servers | Retrieves the collection of GameServer resources.
[**game_servers_restart**](GameServerApi.md#game_servers_restart) | **POST** /api/game_servers/{id}/restart | Creates a GameServer resource.
[**game_servers_start**](GameServerApi.md#game_servers_start) | **POST** /api/game_servers/{id}/start | Creates a GameServer resource.
[**game_servers_stop**](GameServerApi.md#game_servers_stop) | **POST** /api/game_servers/{id}/stop | Creates a GameServer resource.
[**game_servers_update**](GameServerApi.md#game_servers_update) | **PATCH** /api/game_servers/{id} | Updates the GameServer resource.


# **game_servers_create**
> GameServerGameServerRead game_servers_create(game_server_game_server_input)

Creates a GameServer resource.

Creates a GameServer resource.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.game_server_game_server_input import GameServerGameServerInput
from someones_computer_sdk.models.game_server_game_server_read import GameServerGameServerRead
from someones_computer_sdk.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = someones_computer_sdk.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: bearerAuth
configuration = someones_computer_sdk.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with someones_computer_sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = someones_computer_sdk.GameServerApi(api_client)
    game_server_game_server_input = someones_computer_sdk.GameServerGameServerInput() # GameServerGameServerInput | The new GameServer resource

    try:
        # Creates a GameServer resource.
        api_response = api_instance.game_servers_create(game_server_game_server_input)
        print("The response of GameServerApi->game_servers_create:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling GameServerApi->game_servers_create: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **game_server_game_server_input** | [**GameServerGameServerInput**](GameServerGameServerInput.md)| The new GameServer resource | 

### Return type

[**GameServerGameServerRead**](GameServerGameServerRead.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | GameServer resource created |  -  |
**400** | Invalid input |  -  |
**422** | An error occurred |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **game_servers_delete**
> game_servers_delete(id)

Removes the GameServer resource.

Removes the GameServer resource.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = someones_computer_sdk.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: bearerAuth
configuration = someones_computer_sdk.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with someones_computer_sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = someones_computer_sdk.GameServerApi(api_client)
    id = 'id_example' # str | GameServer identifier

    try:
        # Removes the GameServer resource.
        api_instance.game_servers_delete(id)
    except Exception as e:
        print("Exception when calling GameServerApi->game_servers_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| GameServer identifier | 

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json, application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | GameServer resource deleted |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **game_servers_get**
> GameServerGameServerRead game_servers_get(id)

Retrieves a GameServer resource.

Retrieves a GameServer resource.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.game_server_game_server_read import GameServerGameServerRead
from someones_computer_sdk.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = someones_computer_sdk.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: bearerAuth
configuration = someones_computer_sdk.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with someones_computer_sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = someones_computer_sdk.GameServerApi(api_client)
    id = 'id_example' # str | GameServer identifier

    try:
        # Retrieves a GameServer resource.
        api_response = api_instance.game_servers_get(id)
        print("The response of GameServerApi->game_servers_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling GameServerApi->game_servers_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| GameServer identifier | 

### Return type

[**GameServerGameServerRead**](GameServerGameServerRead.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | GameServer resource |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **game_servers_list**
> List[GameServerGameServerRead] game_servers_list(page=page)

Retrieves the collection of GameServer resources.

Retrieves the collection of GameServer resources.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.game_server_game_server_read import GameServerGameServerRead
from someones_computer_sdk.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = someones_computer_sdk.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: bearerAuth
configuration = someones_computer_sdk.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with someones_computer_sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = someones_computer_sdk.GameServerApi(api_client)
    page = 1 # int | The collection page number (optional) (default to 1)

    try:
        # Retrieves the collection of GameServer resources.
        api_response = api_instance.game_servers_list(page=page)
        print("The response of GameServerApi->game_servers_list:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling GameServerApi->game_servers_list: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**| The collection page number | [optional] [default to 1]

### Return type

[**List[GameServerGameServerRead]**](GameServerGameServerRead.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | GameServer collection |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **game_servers_restart**
> GameServerGameServerRead game_servers_restart(id)

Creates a GameServer resource.

Creates a GameServer resource.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.game_server_game_server_read import GameServerGameServerRead
from someones_computer_sdk.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = someones_computer_sdk.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: bearerAuth
configuration = someones_computer_sdk.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with someones_computer_sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = someones_computer_sdk.GameServerApi(api_client)
    id = 'id_example' # str | GameServer identifier

    try:
        # Creates a GameServer resource.
        api_response = api_instance.game_servers_restart(id)
        print("The response of GameServerApi->game_servers_restart:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling GameServerApi->game_servers_restart: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| GameServer identifier | 

### Return type

[**GameServerGameServerRead**](GameServerGameServerRead.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | GameServer resource created |  -  |
**400** | Invalid input |  -  |
**422** | An error occurred |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **game_servers_start**
> GameServerGameServerRead game_servers_start(id)

Creates a GameServer resource.

Creates a GameServer resource.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.game_server_game_server_read import GameServerGameServerRead
from someones_computer_sdk.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = someones_computer_sdk.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: bearerAuth
configuration = someones_computer_sdk.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with someones_computer_sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = someones_computer_sdk.GameServerApi(api_client)
    id = 'id_example' # str | GameServer identifier

    try:
        # Creates a GameServer resource.
        api_response = api_instance.game_servers_start(id)
        print("The response of GameServerApi->game_servers_start:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling GameServerApi->game_servers_start: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| GameServer identifier | 

### Return type

[**GameServerGameServerRead**](GameServerGameServerRead.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | GameServer resource created |  -  |
**400** | Invalid input |  -  |
**422** | An error occurred |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **game_servers_stop**
> GameServerGameServerRead game_servers_stop(id)

Creates a GameServer resource.

Creates a GameServer resource.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.game_server_game_server_read import GameServerGameServerRead
from someones_computer_sdk.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = someones_computer_sdk.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: bearerAuth
configuration = someones_computer_sdk.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with someones_computer_sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = someones_computer_sdk.GameServerApi(api_client)
    id = 'id_example' # str | GameServer identifier

    try:
        # Creates a GameServer resource.
        api_response = api_instance.game_servers_stop(id)
        print("The response of GameServerApi->game_servers_stop:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling GameServerApi->game_servers_stop: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| GameServer identifier | 

### Return type

[**GameServerGameServerRead**](GameServerGameServerRead.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | GameServer resource created |  -  |
**400** | Invalid input |  -  |
**422** | An error occurred |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **game_servers_update**
> GameServerGameServerRead game_servers_update(id, game_server_game_server_settings_input_json_merge_patch)

Updates the GameServer resource.

Updates the GameServer resource.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.game_server_game_server_read import GameServerGameServerRead
from someones_computer_sdk.models.game_server_game_server_settings_input_json_merge_patch import GameServerGameServerSettingsInputJsonMergePatch
from someones_computer_sdk.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = someones_computer_sdk.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: bearerAuth
configuration = someones_computer_sdk.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with someones_computer_sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = someones_computer_sdk.GameServerApi(api_client)
    id = 'id_example' # str | GameServer identifier
    game_server_game_server_settings_input_json_merge_patch = someones_computer_sdk.GameServerGameServerSettingsInputJsonMergePatch() # GameServerGameServerSettingsInputJsonMergePatch | The updated GameServer resource

    try:
        # Updates the GameServer resource.
        api_response = api_instance.game_servers_update(id, game_server_game_server_settings_input_json_merge_patch)
        print("The response of GameServerApi->game_servers_update:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling GameServerApi->game_servers_update: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| GameServer identifier | 
 **game_server_game_server_settings_input_json_merge_patch** | [**GameServerGameServerSettingsInputJsonMergePatch**](GameServerGameServerSettingsInputJsonMergePatch.md)| The updated GameServer resource | 

### Return type

[**GameServerGameServerRead**](GameServerGameServerRead.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/merge-patch+json
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | GameServer resource updated |  -  |
**400** | Invalid input |  -  |
**422** | An error occurred |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

