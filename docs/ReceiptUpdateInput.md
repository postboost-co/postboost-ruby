# PostBoost::ReceiptUpdateInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **transaction_id** | **String** |  |  |
| **invoice_number** | **String** |  |  |
| **amount** | **Float** |  |  |
| **tax** | **Float** |  | [optional] |
| **currency** | **String** |  |  |
| **description** | **String** |  | [optional] |
| **receipt_url** | **String** |  | [optional] |
| **paid_at** | **Date** |  |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::ReceiptUpdateInput.new(
  transaction_id: null,
  invoice_number: null,
  amount: null,
  tax: null,
  currency: null,
  description: null,
  receipt_url: null,
  paid_at: null
)
```

