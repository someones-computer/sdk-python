# CreditTransactionEngineMillis

The engine-milliseconds this load debit was computed from — the delta {@see \\App\\Service\\ManagedService\\LoadSampler} accrued and {@see \\App\\Service\\Credit\\LoadBiller} then billed and cleared. Null on anything but a load debit.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------

## Example

```python
from someones_computer_sdk.models.credit_transaction_engine_millis import CreditTransactionEngineMillis

# TODO update the JSON string below
json = "{}"
# create an instance of CreditTransactionEngineMillis from a JSON string
credit_transaction_engine_millis_instance = CreditTransactionEngineMillis.from_json(json)
# print the JSON string representation of the object
print(CreditTransactionEngineMillis.to_json())

# convert the object into a dict
credit_transaction_engine_millis_dict = credit_transaction_engine_millis_instance.to_dict()
# create an instance of CreditTransactionEngineMillis from a dict
credit_transaction_engine_millis_from_dict = CreditTransactionEngineMillis.from_dict(credit_transaction_engine_millis_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


