# someones_computer_sdk.ApplicationVolumeApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**api_application_volumes_get_collection**](ApplicationVolumeApi.md#api_application_volumes_get_collection) | **GET** /api/application_volumes | Retrieves the collection of ApplicationVolume resources.
[**api_application_volumes_id_delete**](ApplicationVolumeApi.md#api_application_volumes_id_delete) | **DELETE** /api/application_volumes/{id} | Removes the ApplicationVolume resource.
[**api_application_volumes_id_get**](ApplicationVolumeApi.md#api_application_volumes_id_get) | **GET** /api/application_volumes/{id} | Retrieves a ApplicationVolume resource.


# **api_application_volumes_get_collection**
> List[ApplicationVolume] api_application_volumes_get_collection(page=page)

Retrieves the collection of ApplicationVolume resources.

Retrieves the collection of ApplicationVolume resources.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.application_volume import ApplicationVolume
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
    api_instance = someones_computer_sdk.ApplicationVolumeApi(api_client)
    page = 1 # int | The collection page number (optional) (default to 1)

    try:
        # Retrieves the collection of ApplicationVolume resources.
        api_response = api_instance.api_application_volumes_get_collection(page=page)
        print("The response of ApplicationVolumeApi->api_application_volumes_get_collection:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ApplicationVolumeApi->api_application_volumes_get_collection: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**| The collection page number | [optional] [default to 1]

### Return type

[**List[ApplicationVolume]**](ApplicationVolume.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | ApplicationVolume collection |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_application_volumes_id_delete**
> api_application_volumes_id_delete(id)

Removes the ApplicationVolume resource.

Removes the ApplicationVolume resource.

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
    api_instance = someones_computer_sdk.ApplicationVolumeApi(api_client)
    id = 'id_example' # str | ApplicationVolume identifier

    try:
        # Removes the ApplicationVolume resource.
        api_instance.api_application_volumes_id_delete(id)
    except Exception as e:
        print("Exception when calling ApplicationVolumeApi->api_application_volumes_id_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ApplicationVolume identifier | 

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
**204** | ApplicationVolume resource deleted |  -  |
**403** | Forbidden |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_application_volumes_id_get**
> ApplicationVolume api_application_volumes_id_get(id)

Retrieves a ApplicationVolume resource.

Retrieves a ApplicationVolume resource.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.application_volume import ApplicationVolume
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
    api_instance = someones_computer_sdk.ApplicationVolumeApi(api_client)
    id = 'id_example' # str | ApplicationVolume identifier

    try:
        # Retrieves a ApplicationVolume resource.
        api_response = api_instance.api_application_volumes_id_get(id)
        print("The response of ApplicationVolumeApi->api_application_volumes_id_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ApplicationVolumeApi->api_application_volumes_id_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ApplicationVolume identifier | 

### Return type

[**ApplicationVolume**](ApplicationVolume.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | ApplicationVolume resource |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

