# PostBoost::ReceiptInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** |  |  |
| **transaction_id** | **String** |  |  |
| **invoice_number** | **String** |  |  |
| **amount** | **Float** |  |  |
| **tax** | **Float** |  |  |
| **currency** | **String** |  |  |
| **description** | **String** |  | [optional] |
| **receipt_url** | **String** |  | [optional] |
| **paid_at** | **Date** |  |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::ReceiptInput.new(
  workspace_uuid: null,
  transaction_id: null,
  invoice_number: null,
  amount: null,
  tax: null,
  currency: USD,
  description: null,
  receipt_url: null,
  paid_at: null
)
```

