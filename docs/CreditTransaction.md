# CreditTransaction

List an organization's credit ledger rows.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**organization** | **str** |  | [optional] 
**type** | **str** |  | [optional] 
**status** | **str** |  | [optional] [default to 'pending']
**amount_cents** | **int** | Signed integer amount in the smallest currency unit (cents for USD). | [optional] 
**currency** | **str** |  | [optional] [default to 'usd']
**stripe_checkout_session_id** | **str** | Stripe Checkout Session id; a top-up row is created Pending against this before redirecting. Null on a grant and on a debit, neither of which has a Stripe session — the *type* is what says which kind of row this is, not whether this column is set. | [optional] 
**usage_hour** | **datetime** | The clock hour a debit bills for, truncated to the hour and stored UTC. | [optional] [readonly] 
**resource_kind** | **str** | Which meter wrote this row; null on every non-debit row. The other half of the unique key above, and always set on a debit — never left null the way a top-up or grant&#39;s &#x60;usageHour&#x60; is, or two debits from different meters in the same hour would stop colliding with each other but a debit from the *same* meter twice would also stop colliding with itself. | [optional] [readonly] 
**usage_seconds** | **int** | Resolved container-seconds this debit was computed from; null on anything but a compute debit. | [optional] [readonly] 
**unresolved_containers** | **int** | Containers the meter saw start and never saw stop over the billed hour. | [optional] [readonly] 
**usage_bytes** | [**CreditTransactionUsageBytes**](CreditTransactionUsageBytes.md) |  | [optional] 
**engine_millis** | [**CreditTransactionEngineMillis**](CreditTransactionEngineMillis.md) |  | [optional] 
**stripe_event_id** | **str** | Stripe Event id that last transitioned this row; secondary idempotency guard for webhook delivery. | [optional] 
**created_by** | [**User**](User.md) |  | [optional] 
**id** | **str** |  | [optional] [readonly] 
**created_at** | **datetime** |  | [optional] [readonly] 
**updated_at** | **datetime** |  | [optional] [readonly] 

## Example

```python
from someones_computer_sdk.models.credit_transaction import CreditTransaction

# TODO update the JSON string below
json = "{}"
# create an instance of CreditTransaction from a JSON string
credit_transaction_instance = CreditTransaction.from_json(json)
# print the JSON string representation of the object
print(CreditTransaction.to_json())

# convert the object into a dict
credit_transaction_dict = credit_transaction_instance.to_dict()
# create an instance of CreditTransaction from a dict
credit_transaction_from_dict = CreditTransaction.from_dict(credit_transaction_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


