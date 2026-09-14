# someones_computer_sdk.DeploymentAccessGateApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deployment_access_gates_create**](DeploymentAccessGateApi.md#deployment_access_gates_create) | **POST** /api/deployment_access_gates | Creates a DeploymentAccessGate resource.
[**deployment_access_gates_delete**](DeploymentAccessGateApi.md#deployment_access_gates_delete) | **DELETE** /api/deployment_access_gates/{id} | Removes the DeploymentAccessGate resource.
[**deployment_access_gates_get**](DeploymentAccessGateApi.md#deployment_access_gates_get) | **GET** /api/deployment_access_gates/{id} | Retrieves a DeploymentAccessGate resource.
[**deployment_access_gates_list**](DeploymentAccessGateApi.md#deployment_access_gates_list) | **GET** /api/deployment_access_gates | Retrieves the collection of DeploymentAccessGate resources.
[**deployment_access_gates_update**](DeploymentAccessGateApi.md#deployment_access_gates_update) | **PATCH** /api/deployment_access_gates/{id} | Updates the DeploymentAccessGate resource.


# **deployment_access_gates_create**
> DeploymentAccessGate deployment_access_gates_create(deployment_access_gate)

Creates a DeploymentAccessGate resource.

Creates a DeploymentAccessGate resource.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.deployment_access_gate import DeploymentAccessGate
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
    api_instance = someones_computer_sdk.DeploymentAccessGateApi(api_client)
    deployment_access_gate = someones_computer_sdk.DeploymentAccessGate() # DeploymentAccessGate | The new DeploymentAccessGate resource

    try:
        # Creates a DeploymentAccessGate resource.
        api_response = api_instance.deployment_access_gates_create(deployment_access_gate)
        print("The response of DeploymentAccessGateApi->deployment_access_gates_create:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DeploymentAccessGateApi->deployment_access_gates_create: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **deployment_access_gate** | [**DeploymentAccessGate**](DeploymentAccessGate.md)| The new DeploymentAccessGate resource | 

### Return type

[**DeploymentAccessGate**](DeploymentAccessGate.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | DeploymentAccessGate resource created |  -  |
**400** | Invalid input |  -  |
**422** | An error occurred |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deployment_access_gates_delete**
> deployment_access_gates_delete(id)

Removes the DeploymentAccessGate resource.

Removes the DeploymentAccessGate resource.

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
    api_instance = someones_computer_sdk.DeploymentAccessGateApi(api_client)
    id = 'id_example' # str | DeploymentAccessGate identifier

    try:
        # Removes the DeploymentAccessGate resource.
        api_instance.deployment_access_gates_delete(id)
    except Exception as e:
        print("Exception when calling DeploymentAccessGateApi->deployment_access_gates_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| DeploymentAccessGate identifier | 

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
**204** | DeploymentAccessGate resource deleted |  -  |
**403** | Forbidden |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deployment_access_gates_get**
> DeploymentAccessGate deployment_access_gates_get(id)

Retrieves a DeploymentAccessGate resource.

Retrieves a DeploymentAccessGate resource.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.deployment_access_gate import DeploymentAccessGate
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
    api_instance = someones_computer_sdk.DeploymentAccessGateApi(api_client)
    id = 'id_example' # str | DeploymentAccessGate identifier

    try:
        # Retrieves a DeploymentAccessGate resource.
        api_response = api_instance.deployment_access_gates_get(id)
        print("The response of DeploymentAccessGateApi->deployment_access_gates_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DeploymentAccessGateApi->deployment_access_gates_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| DeploymentAccessGate identifier | 

### Return type

[**DeploymentAccessGate**](DeploymentAccessGate.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | DeploymentAccessGate resource |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deployment_access_gates_list**
> List[DeploymentAccessGate] deployment_access_gates_list(page=page)

Retrieves the collection of DeploymentAccessGate resources.

Retrieves the collection of DeploymentAccessGate resources.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.deployment_access_gate import DeploymentAccessGate
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
    api_instance = someones_computer_sdk.DeploymentAccessGateApi(api_client)
    page = 1 # int | The collection page number (optional) (default to 1)

    try:
        # Retrieves the collection of DeploymentAccessGate resources.
        api_response = api_instance.deployment_access_gates_list(page=page)
        print("The response of DeploymentAccessGateApi->deployment_access_gates_list:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DeploymentAccessGateApi->deployment_access_gates_list: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**| The collection page number | [optional] [default to 1]

### Return type

[**List[DeploymentAccessGate]**](DeploymentAccessGate.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | DeploymentAccessGate collection |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deployment_access_gates_update**
> DeploymentAccessGate deployment_access_gates_update(id, deployment_access_gate_json_merge_patch)

Updates the DeploymentAccessGate resource.

Updates the DeploymentAccessGate resource.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.deployment_access_gate import DeploymentAccessGate
from someones_computer_sdk.models.deployment_access_gate_json_merge_patch import DeploymentAccessGateJsonMergePatch
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
    api_instance = someones_computer_sdk.DeploymentAccessGateApi(api_client)
    id = 'id_example' # str | DeploymentAccessGate identifier
    deployment_access_gate_json_merge_patch = someones_computer_sdk.DeploymentAccessGateJsonMergePatch() # DeploymentAccessGateJsonMergePatch | The updated DeploymentAccessGate resource

    try:
        # Updates the DeploymentAccessGate resource.
        api_response = api_instance.deployment_access_gates_update(id, deployment_access_gate_json_merge_patch)
        print("The response of DeploymentAccessGateApi->deployment_access_gates_update:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DeploymentAccessGateApi->deployment_access_gates_update: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| DeploymentAccessGate identifier | 
 **deployment_access_gate_json_merge_patch** | [**DeploymentAccessGateJsonMergePatch**](DeploymentAccessGateJsonMergePatch.md)| The updated DeploymentAccessGate resource | 

### Return type

[**DeploymentAccessGate**](DeploymentAccessGate.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/merge-patch+json
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | DeploymentAccessGate resource updated |  -  |
**400** | Invalid input |  -  |
**422** | An error occurred |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

