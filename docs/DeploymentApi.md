# someones_computer_sdk.DeploymentApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**api_deployments_get_collection**](DeploymentApi.md#api_deployments_get_collection) | **GET** /api/deployments | Retrieves the collection of Deployment resources.
[**api_deployments_id_delete**](DeploymentApi.md#api_deployments_id_delete) | **DELETE** /api/deployments/{id} | Removes the Deployment resource.
[**api_deployments_id_get**](DeploymentApi.md#api_deployments_id_get) | **GET** /api/deployments/{id} | Retrieves a Deployment resource.
[**api_deployments_id_patch**](DeploymentApi.md#api_deployments_id_patch) | **PATCH** /api/deployments/{id} | Updates the Deployment resource.
[**api_deployments_post**](DeploymentApi.md#api_deployments_post) | **POST** /api/deployments | Creates a Deployment resource.


# **api_deployments_get_collection**
> List[Deployment] api_deployments_get_collection(page=page)

Retrieves the collection of Deployment resources.

Retrieves the collection of Deployment resources.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.deployment import Deployment
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
    api_instance = someones_computer_sdk.DeploymentApi(api_client)
    page = 1 # int | The collection page number (optional) (default to 1)

    try:
        # Retrieves the collection of Deployment resources.
        api_response = api_instance.api_deployments_get_collection(page=page)
        print("The response of DeploymentApi->api_deployments_get_collection:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DeploymentApi->api_deployments_get_collection: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**| The collection page number | [optional] [default to 1]

### Return type

[**List[Deployment]**](Deployment.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Deployment collection |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_deployments_id_delete**
> api_deployments_id_delete(id)

Removes the Deployment resource.

Removes the Deployment resource.

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
    api_instance = someones_computer_sdk.DeploymentApi(api_client)
    id = 'id_example' # str | Deployment identifier

    try:
        # Removes the Deployment resource.
        api_instance.api_deployments_id_delete(id)
    except Exception as e:
        print("Exception when calling DeploymentApi->api_deployments_id_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Deployment identifier | 

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
**204** | Deployment resource deleted |  -  |
**403** | Forbidden |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_deployments_id_get**
> Deployment api_deployments_id_get(id)

Retrieves a Deployment resource.

Retrieves a Deployment resource.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.deployment import Deployment
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
    api_instance = someones_computer_sdk.DeploymentApi(api_client)
    id = 'id_example' # str | Deployment identifier

    try:
        # Retrieves a Deployment resource.
        api_response = api_instance.api_deployments_id_get(id)
        print("The response of DeploymentApi->api_deployments_id_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DeploymentApi->api_deployments_id_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Deployment identifier | 

### Return type

[**Deployment**](Deployment.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Deployment resource |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_deployments_id_patch**
> Deployment api_deployments_id_patch(id, deployment_json_merge_patch)

Updates the Deployment resource.

Updates the Deployment resource.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.deployment import Deployment
from someones_computer_sdk.models.deployment_json_merge_patch import DeploymentJsonMergePatch
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
    api_instance = someones_computer_sdk.DeploymentApi(api_client)
    id = 'id_example' # str | Deployment identifier
    deployment_json_merge_patch = someones_computer_sdk.DeploymentJsonMergePatch() # DeploymentJsonMergePatch | The updated Deployment resource

    try:
        # Updates the Deployment resource.
        api_response = api_instance.api_deployments_id_patch(id, deployment_json_merge_patch)
        print("The response of DeploymentApi->api_deployments_id_patch:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DeploymentApi->api_deployments_id_patch: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Deployment identifier | 
 **deployment_json_merge_patch** | [**DeploymentJsonMergePatch**](DeploymentJsonMergePatch.md)| The updated Deployment resource | 

### Return type

[**Deployment**](Deployment.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/merge-patch+json
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Deployment resource updated |  -  |
**400** | Invalid input |  -  |
**422** | An error occurred |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_deployments_post**
> Deployment api_deployments_post(deployment)

Creates a Deployment resource.

Creates a Deployment resource.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.deployment import Deployment
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
    api_instance = someones_computer_sdk.DeploymentApi(api_client)
    deployment = someones_computer_sdk.Deployment() # Deployment | The new Deployment resource

    try:
        # Creates a Deployment resource.
        api_response = api_instance.api_deployments_post(deployment)
        print("The response of DeploymentApi->api_deployments_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DeploymentApi->api_deployments_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **deployment** | [**Deployment**](Deployment.md)| The new Deployment resource | 

### Return type

[**Deployment**](Deployment.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Deployment resource created |  -  |
**400** | Invalid input |  -  |
**422** | An error occurred |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

