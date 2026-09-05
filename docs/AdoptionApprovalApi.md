# someones_computer_sdk.AdoptionApprovalApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**api_adoption_approvals_get_collection**](AdoptionApprovalApi.md#api_adoption_approvals_get_collection) | **GET** /api/adoption_approvals | Retrieves the collection of AdoptionApproval resources.
[**api_adoption_approvals_id_delete**](AdoptionApprovalApi.md#api_adoption_approvals_id_delete) | **DELETE** /api/adoption_approvals/{id} | Removes the AdoptionApproval resource.
[**api_adoption_approvals_id_get**](AdoptionApprovalApi.md#api_adoption_approvals_id_get) | **GET** /api/adoption_approvals/{id} | Retrieves a AdoptionApproval resource.
[**api_adoption_approvals_post**](AdoptionApprovalApi.md#api_adoption_approvals_post) | **POST** /api/adoption_approvals | Creates a AdoptionApproval resource.


# **api_adoption_approvals_get_collection**
> List[AdoptionApproval] api_adoption_approvals_get_collection(page=page)

Retrieves the collection of AdoptionApproval resources.

Retrieves the collection of AdoptionApproval resources.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.adoption_approval import AdoptionApproval
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
    api_instance = someones_computer_sdk.AdoptionApprovalApi(api_client)
    page = 1 # int | The collection page number (optional) (default to 1)

    try:
        # Retrieves the collection of AdoptionApproval resources.
        api_response = api_instance.api_adoption_approvals_get_collection(page=page)
        print("The response of AdoptionApprovalApi->api_adoption_approvals_get_collection:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AdoptionApprovalApi->api_adoption_approvals_get_collection: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**| The collection page number | [optional] [default to 1]

### Return type

[**List[AdoptionApproval]**](AdoptionApproval.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | AdoptionApproval collection |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_adoption_approvals_id_delete**
> api_adoption_approvals_id_delete(id)

Removes the AdoptionApproval resource.

Removes the AdoptionApproval resource.

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
    api_instance = someones_computer_sdk.AdoptionApprovalApi(api_client)
    id = 'id_example' # str | AdoptionApproval identifier

    try:
        # Removes the AdoptionApproval resource.
        api_instance.api_adoption_approvals_id_delete(id)
    except Exception as e:
        print("Exception when calling AdoptionApprovalApi->api_adoption_approvals_id_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| AdoptionApproval identifier | 

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
**204** | AdoptionApproval resource deleted |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_adoption_approvals_id_get**
> AdoptionApproval api_adoption_approvals_id_get(id)

Retrieves a AdoptionApproval resource.

Retrieves a AdoptionApproval resource.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.adoption_approval import AdoptionApproval
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
    api_instance = someones_computer_sdk.AdoptionApprovalApi(api_client)
    id = 'id_example' # str | AdoptionApproval identifier

    try:
        # Retrieves a AdoptionApproval resource.
        api_response = api_instance.api_adoption_approvals_id_get(id)
        print("The response of AdoptionApprovalApi->api_adoption_approvals_id_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AdoptionApprovalApi->api_adoption_approvals_id_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| AdoptionApproval identifier | 

### Return type

[**AdoptionApproval**](AdoptionApproval.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | AdoptionApproval resource |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_adoption_approvals_post**
> AdoptionApproval api_adoption_approvals_post(adoption_approval_adoption_approval_input)

Creates a AdoptionApproval resource.

Creates a AdoptionApproval resource.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.adoption_approval import AdoptionApproval
from someones_computer_sdk.models.adoption_approval_adoption_approval_input import AdoptionApprovalAdoptionApprovalInput
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
    api_instance = someones_computer_sdk.AdoptionApprovalApi(api_client)
    adoption_approval_adoption_approval_input = someones_computer_sdk.AdoptionApprovalAdoptionApprovalInput() # AdoptionApprovalAdoptionApprovalInput | The new AdoptionApproval resource

    try:
        # Creates a AdoptionApproval resource.
        api_response = api_instance.api_adoption_approvals_post(adoption_approval_adoption_approval_input)
        print("The response of AdoptionApprovalApi->api_adoption_approvals_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AdoptionApprovalApi->api_adoption_approvals_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **adoption_approval_adoption_approval_input** | [**AdoptionApprovalAdoptionApprovalInput**](AdoptionApprovalAdoptionApprovalInput.md)| The new AdoptionApproval resource | 

### Return type

[**AdoptionApproval**](AdoptionApproval.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | AdoptionApproval resource created |  -  |
**400** | Invalid input |  -  |
**422** | An error occurred |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

