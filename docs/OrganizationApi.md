# someones_computer_sdk.OrganizationApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**api_organizations_get_collection**](OrganizationApi.md#api_organizations_get_collection) | **GET** /api/organizations | Retrieves the collection of Organization resources.
[**api_organizations_id_delete**](OrganizationApi.md#api_organizations_id_delete) | **DELETE** /api/organizations/{id} | Removes the Organization resource.
[**api_organizations_id_get**](OrganizationApi.md#api_organizations_id_get) | **GET** /api/organizations/{id} | Retrieves a Organization resource.
[**api_organizations_id_patch**](OrganizationApi.md#api_organizations_id_patch) | **PATCH** /api/organizations/{id} | Updates the Organization resource.
[**api_organizations_post**](OrganizationApi.md#api_organizations_post) | **POST** /api/organizations | Creates a Organization resource.


# **api_organizations_get_collection**
> List[Organization] api_organizations_get_collection(page=page, slug=slug, slug2=slug2)

Retrieves the collection of Organization resources.

Retrieves the collection of Organization resources.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.organization import Organization
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
    api_instance = someones_computer_sdk.OrganizationApi(api_client)
    page = 1 # int | The collection page number (optional) (default to 1)
    slug = 'slug_example' # str |  (optional)
    slug2 = ['slug_example'] # List[str] |  (optional)

    try:
        # Retrieves the collection of Organization resources.
        api_response = api_instance.api_organizations_get_collection(page=page, slug=slug, slug2=slug2)
        print("The response of OrganizationApi->api_organizations_get_collection:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrganizationApi->api_organizations_get_collection: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**| The collection page number | [optional] [default to 1]
 **slug** | **str**|  | [optional] 
 **slug2** | [**List[str]**](str.md)|  | [optional] 

### Return type

[**List[Organization]**](Organization.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Organization collection |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_organizations_id_delete**
> api_organizations_id_delete(id)

Removes the Organization resource.

Removes the Organization resource.

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
    api_instance = someones_computer_sdk.OrganizationApi(api_client)
    id = 'id_example' # str | Organization identifier

    try:
        # Removes the Organization resource.
        api_instance.api_organizations_id_delete(id)
    except Exception as e:
        print("Exception when calling OrganizationApi->api_organizations_id_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Organization identifier | 

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
**204** | Organization resource deleted |  -  |
**403** | Forbidden |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_organizations_id_get**
> Organization api_organizations_id_get(id)

Retrieves a Organization resource.

Retrieves a Organization resource.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.organization import Organization
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
    api_instance = someones_computer_sdk.OrganizationApi(api_client)
    id = 'id_example' # str | Organization identifier

    try:
        # Retrieves a Organization resource.
        api_response = api_instance.api_organizations_id_get(id)
        print("The response of OrganizationApi->api_organizations_id_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrganizationApi->api_organizations_id_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Organization identifier | 

### Return type

[**Organization**](Organization.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Organization resource |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_organizations_id_patch**
> Organization api_organizations_id_patch(id, organization_json_merge_patch)

Updates the Organization resource.

Updates the Organization resource.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.organization import Organization
from someones_computer_sdk.models.organization_json_merge_patch import OrganizationJsonMergePatch
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
    api_instance = someones_computer_sdk.OrganizationApi(api_client)
    id = 'id_example' # str | Organization identifier
    organization_json_merge_patch = someones_computer_sdk.OrganizationJsonMergePatch() # OrganizationJsonMergePatch | The updated Organization resource

    try:
        # Updates the Organization resource.
        api_response = api_instance.api_organizations_id_patch(id, organization_json_merge_patch)
        print("The response of OrganizationApi->api_organizations_id_patch:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrganizationApi->api_organizations_id_patch: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Organization identifier | 
 **organization_json_merge_patch** | [**OrganizationJsonMergePatch**](OrganizationJsonMergePatch.md)| The updated Organization resource | 

### Return type

[**Organization**](Organization.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/merge-patch+json
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Organization resource updated |  -  |
**400** | Invalid input |  -  |
**422** | An error occurred |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_organizations_post**
> Organization api_organizations_post(organization)

Creates a Organization resource.

Creates a Organization resource.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.organization import Organization
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
    api_instance = someones_computer_sdk.OrganizationApi(api_client)
    organization = someones_computer_sdk.Organization() # Organization | The new Organization resource

    try:
        # Creates a Organization resource.
        api_response = api_instance.api_organizations_post(organization)
        print("The response of OrganizationApi->api_organizations_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrganizationApi->api_organizations_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | [**Organization**](Organization.md)| The new Organization resource | 

### Return type

[**Organization**](Organization.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Organization resource created |  -  |
**400** | Invalid input |  -  |
**422** | An error occurred |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

