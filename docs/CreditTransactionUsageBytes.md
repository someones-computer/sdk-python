# CreditTransactionUsageBytes

The byte snapshot a storage debit was computed from — the evidence a GiB-month charge can be checked against, the same role {@see $usageSeconds} plays for a compute debit. Null on anything but a storage debit.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------

## Example

```python
from someones_computer_sdk.models.credit_transaction_usage_bytes import CreditTransactionUsageBytes

# TODO update the JSON string below
json = "{}"
# create an instance of CreditTransactionUsageBytes from a JSON string
credit_transaction_usage_bytes_instance = CreditTransactionUsageBytes.from_json(json)
# print the JSON string representation of the object
print(CreditTransactionUsageBytes.to_json())

# convert the object into a dict
credit_transaction_usage_bytes_dict = credit_transaction_usage_bytes_instance.to_dict()
# create an instance of CreditTransactionUsageBytes from a dict
credit_transaction_usage_bytes_from_dict = CreditTransactionUsageBytes.from_dict(credit_transaction_usage_bytes_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


