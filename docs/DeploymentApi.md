# someones_computer_sdk.DeploymentApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deployments_bundle_upload_confirm**](DeploymentApi.md#deployments_bundle_upload_confirm) | **POST** /api/deployments/bundle_uploads/confirm | Creates a Deployment resource.
[**deployments_bundle_upload_declare**](DeploymentApi.md#deployments_bundle_upload_declare) | **POST** /api/deployments/bundle_uploads | Creates a Deployment resource.
[**deployments_create**](DeploymentApi.md#deployments_create) | **POST** /api/deployments | Creates a Deployment resource.
[**deployments_delete**](DeploymentApi.md#deployments_delete) | **DELETE** /api/deployments/{id} | Removes the Deployment resource.
[**deployments_endpoints**](DeploymentApi.md#deployments_endpoints) | **GET** /api/deployments/{id}/endpoints | Retrieves the collection of Deployment resources.
[**deployments_get**](DeploymentApi.md#deployments_get) | **GET** /api/deployments/{id} | Retrieves a Deployment resource.
[**deployments_list**](DeploymentApi.md#deployments_list) | **GET** /api/deployments | Retrieves the collection of Deployment resources.
[**deployments_update**](DeploymentApi.md#deployments_update) | **PATCH** /api/deployments/{id} | Updates the Deployment resource.


# **deployments_bundle_upload_confirm**
> DeploymentBundleUploadConfirmOutput deployments_bundle_upload_confirm(deployment_bundle_upload_confirm_input)

Creates a Deployment resource.

Creates a Deployment resource.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.deployment_bundle_upload_confirm_input import DeploymentBundleUploadConfirmInput
from someones_computer_sdk.models.deployment_bundle_upload_confirm_output import DeploymentBundleUploadConfirmOutput
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
    deployment_bundle_upload_confirm_input = someones_computer_sdk.DeploymentBundleUploadConfirmInput() # DeploymentBundleUploadConfirmInput | The new Deployment resource

    try:
        # Creates a Deployment resource.
        api_response = api_instance.deployments_bundle_upload_confirm(deployment_bundle_upload_confirm_input)
        print("The response of DeploymentApi->deployments_bundle_upload_confirm:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DeploymentApi->deployments_bundle_upload_confirm: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **deployment_bundle_upload_confirm_input** | [**DeploymentBundleUploadConfirmInput**](DeploymentBundleUploadConfirmInput.md)| The new Deployment resource | 

### Return type

[**DeploymentBundleUploadConfirmOutput**](DeploymentBundleUploadConfirmOutput.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Deployment resource created |  -  |
**400** | Invalid input |  -  |
**422** | An error occurred |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deployments_bundle_upload_declare**
> DeploymentBundleUploadDeclareOutput deployments_bundle_upload_declare(deployment_bundle_upload_declare_input)

Creates a Deployment resource.

Creates a Deployment resource.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.deployment_bundle_upload_declare_input import DeploymentBundleUploadDeclareInput
from someones_computer_sdk.models.deployment_bundle_upload_declare_output import DeploymentBundleUploadDeclareOutput
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
    deployment_bundle_upload_declare_input = someones_computer_sdk.DeploymentBundleUploadDeclareInput() # DeploymentBundleUploadDeclareInput | The new Deployment resource

    try:
        # Creates a Deployment resource.
        api_response = api_instance.deployments_bundle_upload_declare(deployment_bundle_upload_declare_input)
        print("The response of DeploymentApi->deployments_bundle_upload_declare:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DeploymentApi->deployments_bundle_upload_declare: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **deployment_bundle_upload_declare_input** | [**DeploymentBundleUploadDeclareInput**](DeploymentBundleUploadDeclareInput.md)| The new Deployment resource | 

### Return type

[**DeploymentBundleUploadDeclareOutput**](DeploymentBundleUploadDeclareOutput.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Deployment resource created |  -  |
**400** | Invalid input |  -  |
**422** | An error occurred |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deployments_create**
> Deployment deployments_create(deployment)

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
        api_response = api_instance.deployments_create(deployment)
        print("The response of DeploymentApi->deployments_create:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DeploymentApi->deployments_create: %s\n" % e)
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

# **deployments_delete**
> deployments_delete(id)

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
        api_instance.deployments_delete(id)
    except Exception as e:
        print("Exception when calling DeploymentApi->deployments_delete: %s\n" % e)
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

# **deployments_endpoints**
> List[DeploymentDeploymentEndpoint] deployments_endpoints(id)

Retrieves the collection of Deployment resources.

Retrieves the collection of Deployment resources.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.deployment_deployment_endpoint import DeploymentDeploymentEndpoint
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
        # Retrieves the collection of Deployment resources.
        api_response = api_instance.deployments_endpoints(id)
        print("The response of DeploymentApi->deployments_endpoints:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DeploymentApi->deployments_endpoints: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Deployment identifier | 

### Return type

[**List[DeploymentDeploymentEndpoint]**](DeploymentDeploymentEndpoint.md)

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

# **deployments_get**
> Deployment deployments_get(id)

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
        api_response = api_instance.deployments_get(id)
        print("The response of DeploymentApi->deployments_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DeploymentApi->deployments_get: %s\n" % e)
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

# **deployments_list**
> List[Deployment] deployments_list(page=page)

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
        api_response = api_instance.deployments_list(page=page)
        print("The response of DeploymentApi->deployments_list:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DeploymentApi->deployments_list: %s\n" % e)
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

# **deployments_update**
> Deployment deployments_update(id, deployment_json_merge_patch)

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
        api_response = api_instance.deployments_update(id, deployment_json_merge_patch)
        print("The response of DeploymentApi->deployments_update:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DeploymentApi->deployments_update: %s\n" % e)
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

