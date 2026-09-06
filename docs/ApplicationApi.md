# someones_computer_sdk.ApplicationApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**api_applications_get_collection**](ApplicationApi.md#api_applications_get_collection) | **GET** /api/applications | Retrieves the collection of Application resources.
[**api_applications_id_delete**](ApplicationApi.md#api_applications_id_delete) | **DELETE** /api/applications/{id} | Removes the Application resource.
[**api_applications_id_get**](ApplicationApi.md#api_applications_id_get) | **GET** /api/applications/{id} | Retrieves a Application resource.
[**api_applications_id_patch**](ApplicationApi.md#api_applications_id_patch) | **PATCH** /api/applications/{id} | Updates the Application resource.
[**api_applications_post**](ApplicationApi.md#api_applications_post) | **POST** /api/applications | Creates a Application resource.


# **api_applications_get_collection**
> List[Application] api_applications_get_collection(page=page, slug=slug, slug2=slug2, organization=organization, organization2=organization2, organization_slug=organization_slug, organization_slug2=organization_slug2)

Retrieves the collection of Application resources.

Retrieves the collection of Application resources.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.application import Application
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
    api_instance = someones_computer_sdk.ApplicationApi(api_client)
    page = 1 # int | The collection page number (optional) (default to 1)
    slug = 'slug_example' # str |  (optional)
    slug2 = ['slug_example'] # List[str] |  (optional)
    organization = 'organization_example' # str |  (optional)
    organization2 = ['organization_example'] # List[str] |  (optional)
    organization_slug = 'organization_slug_example' # str |  (optional)
    organization_slug2 = ['organization_slug_example'] # List[str] |  (optional)

    try:
        # Retrieves the collection of Application resources.
        api_response = api_instance.api_applications_get_collection(page=page, slug=slug, slug2=slug2, organization=organization, organization2=organization2, organization_slug=organization_slug, organization_slug2=organization_slug2)
        print("The response of ApplicationApi->api_applications_get_collection:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ApplicationApi->api_applications_get_collection: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**| The collection page number | [optional] [default to 1]
 **slug** | **str**|  | [optional] 
 **slug2** | [**List[str]**](str.md)|  | [optional] 
 **organization** | **str**|  | [optional] 
 **organization2** | [**List[str]**](str.md)|  | [optional] 
 **organization_slug** | **str**|  | [optional] 
 **organization_slug2** | [**List[str]**](str.md)|  | [optional] 

### Return type

[**List[Application]**](Application.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Application collection |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_applications_id_delete**
> api_applications_id_delete(id)

Removes the Application resource.

Removes the Application resource.

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
    api_instance = someones_computer_sdk.ApplicationApi(api_client)
    id = 'id_example' # str | Application identifier

    try:
        # Removes the Application resource.
        api_instance.api_applications_id_delete(id)
    except Exception as e:
        print("Exception when calling ApplicationApi->api_applications_id_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Application identifier | 

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
**204** | Application resource deleted |  -  |
**403** | Forbidden |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_applications_id_get**
> Application api_applications_id_get(id)

Retrieves a Application resource.

Retrieves a Application resource.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.application import Application
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
    api_instance = someones_computer_sdk.ApplicationApi(api_client)
    id = 'id_example' # str | Application identifier

    try:
        # Retrieves a Application resource.
        api_response = api_instance.api_applications_id_get(id)
        print("The response of ApplicationApi->api_applications_id_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ApplicationApi->api_applications_id_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Application identifier | 

### Return type

[**Application**](Application.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Application resource |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_applications_id_patch**
> Application api_applications_id_patch(id, application_json_merge_patch)

Updates the Application resource.

Updates the Application resource.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.application import Application
from someones_computer_sdk.models.application_json_merge_patch import ApplicationJsonMergePatch
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
    api_instance = someones_computer_sdk.ApplicationApi(api_client)
    id = 'id_example' # str | Application identifier
    application_json_merge_patch = someones_computer_sdk.ApplicationJsonMergePatch() # ApplicationJsonMergePatch | The updated Application resource

    try:
        # Updates the Application resource.
        api_response = api_instance.api_applications_id_patch(id, application_json_merge_patch)
        print("The response of ApplicationApi->api_applications_id_patch:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ApplicationApi->api_applications_id_patch: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Application identifier | 
 **application_json_merge_patch** | [**ApplicationJsonMergePatch**](ApplicationJsonMergePatch.md)| The updated Application resource | 

### Return type

[**Application**](Application.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/merge-patch+json
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Application resource updated |  -  |
**400** | Invalid input |  -  |
**422** | An error occurred |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_applications_post**
> Application api_applications_post(application)

Creates a Application resource.

Creates a Application resource.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.application import Application
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
    api_instance = someones_computer_sdk.ApplicationApi(api_client)
    application = someones_computer_sdk.Application() # Application | The new Application resource

    try:
        # Creates a Application resource.
        api_response = api_instance.api_applications_post(application)
        print("The response of ApplicationApi->api_applications_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ApplicationApi->api_applications_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **application** | [**Application**](Application.md)| The new Application resource | 

### Return type

[**Application**](Application.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Application resource created |  -  |
**400** | Invalid input |  -  |
**422** | An error occurred |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

