# someones_computer_sdk.ManagedServiceApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**api_managed_services_get_collection**](ManagedServiceApi.md#api_managed_services_get_collection) | **GET** /api/managed_services | Retrieves the collection of ManagedService resources.
[**api_managed_services_id_delete**](ManagedServiceApi.md#api_managed_services_id_delete) | **DELETE** /api/managed_services/{id} | Removes the ManagedService resource.
[**api_managed_services_id_get**](ManagedServiceApi.md#api_managed_services_id_get) | **GET** /api/managed_services/{id} | Retrieves a ManagedService resource.
[**api_managed_services_post**](ManagedServiceApi.md#api_managed_services_post) | **POST** /api/managed_services | Creates a ManagedService resource.
[**resume**](ManagedServiceApi.md#resume) | **POST** /api/managed_services/{id}/resume | Creates a ManagedService resource.
[**suspend**](ManagedServiceApi.md#suspend) | **POST** /api/managed_services/{id}/suspend | Creates a ManagedService resource.


# **api_managed_services_get_collection**
> List[ManagedService] api_managed_services_get_collection(page=page)

Retrieves the collection of ManagedService resources.

Retrieves the collection of ManagedService resources.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.managed_service import ManagedService
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
    api_instance = someones_computer_sdk.ManagedServiceApi(api_client)
    page = 1 # int | The collection page number (optional) (default to 1)

    try:
        # Retrieves the collection of ManagedService resources.
        api_response = api_instance.api_managed_services_get_collection(page=page)
        print("The response of ManagedServiceApi->api_managed_services_get_collection:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ManagedServiceApi->api_managed_services_get_collection: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**| The collection page number | [optional] [default to 1]

### Return type

[**List[ManagedService]**](ManagedService.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | ManagedService collection |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_managed_services_id_delete**
> api_managed_services_id_delete(id)

Removes the ManagedService resource.

Removes the ManagedService resource.

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
    api_instance = someones_computer_sdk.ManagedServiceApi(api_client)
    id = 'id_example' # str | ManagedService identifier

    try:
        # Removes the ManagedService resource.
        api_instance.api_managed_services_id_delete(id)
    except Exception as e:
        print("Exception when calling ManagedServiceApi->api_managed_services_id_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ManagedService identifier | 

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
**204** | ManagedService resource deleted |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_managed_services_id_get**
> ManagedService api_managed_services_id_get(id)

Retrieves a ManagedService resource.

Retrieves a ManagedService resource.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.managed_service import ManagedService
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
    api_instance = someones_computer_sdk.ManagedServiceApi(api_client)
    id = 'id_example' # str | ManagedService identifier

    try:
        # Retrieves a ManagedService resource.
        api_response = api_instance.api_managed_services_id_get(id)
        print("The response of ManagedServiceApi->api_managed_services_id_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ManagedServiceApi->api_managed_services_id_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ManagedService identifier | 

### Return type

[**ManagedService**](ManagedService.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | ManagedService resource |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_managed_services_post**
> ManagedService api_managed_services_post(managed_service_managed_service_input)

Creates a ManagedService resource.

Creates a ManagedService resource.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.managed_service import ManagedService
from someones_computer_sdk.models.managed_service_managed_service_input import ManagedServiceManagedServiceInput
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
    api_instance = someones_computer_sdk.ManagedServiceApi(api_client)
    managed_service_managed_service_input = someones_computer_sdk.ManagedServiceManagedServiceInput() # ManagedServiceManagedServiceInput | The new ManagedService resource

    try:
        # Creates a ManagedService resource.
        api_response = api_instance.api_managed_services_post(managed_service_managed_service_input)
        print("The response of ManagedServiceApi->api_managed_services_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ManagedServiceApi->api_managed_services_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **managed_service_managed_service_input** | [**ManagedServiceManagedServiceInput**](ManagedServiceManagedServiceInput.md)| The new ManagedService resource | 

### Return type

[**ManagedService**](ManagedService.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | ManagedService resource created |  -  |
**400** | Invalid input |  -  |
**422** | An error occurred |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **resume**
> ManagedService resume(id)

Creates a ManagedService resource.

Creates a ManagedService resource.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.managed_service import ManagedService
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
    api_instance = someones_computer_sdk.ManagedServiceApi(api_client)
    id = 'id_example' # str | ManagedService identifier

    try:
        # Creates a ManagedService resource.
        api_response = api_instance.resume(id)
        print("The response of ManagedServiceApi->resume:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ManagedServiceApi->resume: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ManagedService identifier | 

### Return type

[**ManagedService**](ManagedService.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | ManagedService resource created |  -  |
**400** | Invalid input |  -  |
**422** | An error occurred |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **suspend**
> ManagedService suspend(id)

Creates a ManagedService resource.

Creates a ManagedService resource.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.managed_service import ManagedService
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
    api_instance = someones_computer_sdk.ManagedServiceApi(api_client)
    id = 'id_example' # str | ManagedService identifier

    try:
        # Creates a ManagedService resource.
        api_response = api_instance.suspend(id)
        print("The response of ManagedServiceApi->suspend:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ManagedServiceApi->suspend: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ManagedService identifier | 

### Return type

[**ManagedService**](ManagedService.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | ManagedService resource created |  -  |
**400** | Invalid input |  -  |
**422** | An error occurred |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

