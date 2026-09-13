# someones_computer_sdk.CreditTransactionApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**credit_transactions_get**](CreditTransactionApi.md#credit_transactions_get) | **GET** /api/credit_transactions/{id} | Retrieves a CreditTransaction resource.
[**credit_transactions_list**](CreditTransactionApi.md#credit_transactions_list) | **GET** /api/credit_transactions | Retrieves the collection of CreditTransaction resources.


# **credit_transactions_get**
> CreditTransaction credit_transactions_get(id)

Retrieves a CreditTransaction resource.

Retrieves a CreditTransaction resource.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.credit_transaction import CreditTransaction
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
    api_instance = someones_computer_sdk.CreditTransactionApi(api_client)
    id = 'id_example' # str | CreditTransaction identifier

    try:
        # Retrieves a CreditTransaction resource.
        api_response = api_instance.credit_transactions_get(id)
        print("The response of CreditTransactionApi->credit_transactions_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CreditTransactionApi->credit_transactions_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| CreditTransaction identifier | 

### Return type

[**CreditTransaction**](CreditTransaction.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | CreditTransaction resource |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **credit_transactions_list**
> List[CreditTransaction] credit_transactions_list(page=page)

Retrieves the collection of CreditTransaction resources.

Retrieves the collection of CreditTransaction resources.

### Example

* Bearer Authentication (bearerAuth):

```python
import someones_computer_sdk
from someones_computer_sdk.models.credit_transaction import CreditTransaction
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
    api_instance = someones_computer_sdk.CreditTransactionApi(api_client)
    page = 1 # int | The collection page number (optional) (default to 1)

    try:
        # Retrieves the collection of CreditTransaction resources.
        api_response = api_instance.credit_transactions_list(page=page)
        print("The response of CreditTransactionApi->credit_transactions_list:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CreditTransactionApi->credit_transactions_list: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**| The collection page number | [optional] [default to 1]

### Return type

[**List[CreditTransaction]**](CreditTransaction.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | CreditTransaction collection |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

