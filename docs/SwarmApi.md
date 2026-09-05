# someones_computer_sdk.SwarmApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**api_swarms_get_collection**](SwarmApi.md#api_swarms_get_collection) | **GET** /api/swarms | Retrieves the collection of Swarm resources.
[**api_swarms_id_delete**](SwarmApi.md#api_swarms_id_delete) | **DELETE** /api/swarms/{id} | Removes the Swarm resource.
[**api_swarms_id_get**](SwarmApi.md#api_swarms_id_get) | **GET** /api/swarms/{id} | Retrieves a Swarm resource.
[**api_swarms_id_patch**](SwarmApi.md#api_swarms_id_patch) | **PATCH** /api/swarms/{id} | Updates the Swarm resource.
[**api_swarms_post**](SwarmApi.md#api_swarms_post) | **POST** /api/swarms | Creates a Swarm resource.


# **api_swarms_get_collection**
> List[Swarm] api_swarms_get_collection(page=page)

Retrieves the collection of Swarm resources.

Retrieves the collection of Swarm resources.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.swarm import Swarm
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
    api_instance = someones_computer_sdk.SwarmApi(api_client)
    page = 1 # int | The collection page number (optional) (default to 1)

    try:
        # Retrieves the collection of Swarm resources.
        api_response = api_instance.api_swarms_get_collection(page=page)
        print("The response of SwarmApi->api_swarms_get_collection:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SwarmApi->api_swarms_get_collection: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**| The collection page number | [optional] [default to 1]

### Return type

[**List[Swarm]**](Swarm.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Swarm collection |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_swarms_id_delete**
> api_swarms_id_delete(id)

Removes the Swarm resource.

Removes the Swarm resource.

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
    api_instance = someones_computer_sdk.SwarmApi(api_client)
    id = 'id_example' # str | Swarm identifier

    try:
        # Removes the Swarm resource.
        api_instance.api_swarms_id_delete(id)
    except Exception as e:
        print("Exception when calling SwarmApi->api_swarms_id_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Swarm identifier | 

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
**204** | Swarm resource deleted |  -  |
**403** | Forbidden |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_swarms_id_get**
> Swarm api_swarms_id_get(id)

Retrieves a Swarm resource.

Retrieves a Swarm resource.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.swarm import Swarm
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
    api_instance = someones_computer_sdk.SwarmApi(api_client)
    id = 'id_example' # str | Swarm identifier

    try:
        # Retrieves a Swarm resource.
        api_response = api_instance.api_swarms_id_get(id)
        print("The response of SwarmApi->api_swarms_id_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SwarmApi->api_swarms_id_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Swarm identifier | 

### Return type

[**Swarm**](Swarm.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Swarm resource |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_swarms_id_patch**
> Swarm api_swarms_id_patch(id, swarm_json_merge_patch)

Updates the Swarm resource.

Updates the Swarm resource.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.swarm import Swarm
from someones_computer_sdk.models.swarm_json_merge_patch import SwarmJsonMergePatch
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
    api_instance = someones_computer_sdk.SwarmApi(api_client)
    id = 'id_example' # str | Swarm identifier
    swarm_json_merge_patch = someones_computer_sdk.SwarmJsonMergePatch() # SwarmJsonMergePatch | The updated Swarm resource

    try:
        # Updates the Swarm resource.
        api_response = api_instance.api_swarms_id_patch(id, swarm_json_merge_patch)
        print("The response of SwarmApi->api_swarms_id_patch:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SwarmApi->api_swarms_id_patch: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Swarm identifier | 
 **swarm_json_merge_patch** | [**SwarmJsonMergePatch**](SwarmJsonMergePatch.md)| The updated Swarm resource | 

### Return type

[**Swarm**](Swarm.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/merge-patch+json
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Swarm resource updated |  -  |
**400** | Invalid input |  -  |
**422** | An error occurred |  -  |
**403** | Forbidden |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_swarms_post**
> Swarm api_swarms_post(swarm)

Creates a Swarm resource.

Creates a Swarm resource.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.swarm import Swarm
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
    api_instance = someones_computer_sdk.SwarmApi(api_client)
    swarm = someones_computer_sdk.Swarm() # Swarm | The new Swarm resource

    try:
        # Creates a Swarm resource.
        api_response = api_instance.api_swarms_post(swarm)
        print("The response of SwarmApi->api_swarms_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SwarmApi->api_swarms_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **swarm** | [**Swarm**](Swarm.md)| The new Swarm resource | 

### Return type

[**Swarm**](Swarm.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Swarm resource created |  -  |
**400** | Invalid input |  -  |
**422** | An error occurred |  -  |
**403** | Forbidden |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

