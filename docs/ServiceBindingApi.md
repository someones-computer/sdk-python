# someones_computer_sdk.ServiceBindingApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**api_service_bindings_get_collection**](ServiceBindingApi.md#api_service_bindings_get_collection) | **GET** /api/service_bindings | Retrieves the collection of ServiceBinding resources.
[**api_service_bindings_id_delete**](ServiceBindingApi.md#api_service_bindings_id_delete) | **DELETE** /api/service_bindings/{id} | Removes the ServiceBinding resource.
[**api_service_bindings_id_get**](ServiceBindingApi.md#api_service_bindings_id_get) | **GET** /api/service_bindings/{id} | Retrieves a ServiceBinding resource.
[**api_service_bindings_post**](ServiceBindingApi.md#api_service_bindings_post) | **POST** /api/service_bindings | Creates a ServiceBinding resource.


# **api_service_bindings_get_collection**
> List[ServiceBinding] api_service_bindings_get_collection(page=page)

Retrieves the collection of ServiceBinding resources.

Retrieves the collection of ServiceBinding resources.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.service_binding import ServiceBinding
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
    api_instance = someones_computer_sdk.ServiceBindingApi(api_client)
    page = 1 # int | The collection page number (optional) (default to 1)

    try:
        # Retrieves the collection of ServiceBinding resources.
        api_response = api_instance.api_service_bindings_get_collection(page=page)
        print("The response of ServiceBindingApi->api_service_bindings_get_collection:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServiceBindingApi->api_service_bindings_get_collection: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**| The collection page number | [optional] [default to 1]

### Return type

[**List[ServiceBinding]**](ServiceBinding.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | ServiceBinding collection |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_service_bindings_id_delete**
> api_service_bindings_id_delete(id)

Removes the ServiceBinding resource.

Removes the ServiceBinding resource.

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
    api_instance = someones_computer_sdk.ServiceBindingApi(api_client)
    id = 'id_example' # str | ServiceBinding identifier

    try:
        # Removes the ServiceBinding resource.
        api_instance.api_service_bindings_id_delete(id)
    except Exception as e:
        print("Exception when calling ServiceBindingApi->api_service_bindings_id_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ServiceBinding identifier | 

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
**204** | ServiceBinding resource deleted |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_service_bindings_id_get**
> ServiceBinding api_service_bindings_id_get(id)

Retrieves a ServiceBinding resource.

Retrieves a ServiceBinding resource.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.service_binding import ServiceBinding
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
    api_instance = someones_computer_sdk.ServiceBindingApi(api_client)
    id = 'id_example' # str | ServiceBinding identifier

    try:
        # Retrieves a ServiceBinding resource.
        api_response = api_instance.api_service_bindings_id_get(id)
        print("The response of ServiceBindingApi->api_service_bindings_id_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServiceBindingApi->api_service_bindings_id_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ServiceBinding identifier | 

### Return type

[**ServiceBinding**](ServiceBinding.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | ServiceBinding resource |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_service_bindings_post**
> ServiceBinding api_service_bindings_post(service_binding_service_binding_input)

Creates a ServiceBinding resource.

Creates a ServiceBinding resource.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.service_binding import ServiceBinding
from someones_computer_sdk.models.service_binding_service_binding_input import ServiceBindingServiceBindingInput
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
    api_instance = someones_computer_sdk.ServiceBindingApi(api_client)
    service_binding_service_binding_input = someones_computer_sdk.ServiceBindingServiceBindingInput() # ServiceBindingServiceBindingInput | The new ServiceBinding resource

    try:
        # Creates a ServiceBinding resource.
        api_response = api_instance.api_service_bindings_post(service_binding_service_binding_input)
        print("The response of ServiceBindingApi->api_service_bindings_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ServiceBindingApi->api_service_bindings_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **service_binding_service_binding_input** | [**ServiceBindingServiceBindingInput**](ServiceBindingServiceBindingInput.md)| The new ServiceBinding resource | 

### Return type

[**ServiceBinding**](ServiceBinding.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | ServiceBinding resource created |  -  |
**400** | Invalid input |  -  |
**422** | An error occurred |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

