# PostBoost::Receipt

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **uuid** | **String** |  |  |
| **transaction_id** | **String** |  |  |
| **invoice_number** | **String** |  |  |
| **amount** | **Float** |  |  |
| **tax** | **Float** |  |  |
| **currency** | **String** |  |  |
| **receipt_url** | **String** |  | [optional] |
| **description** | **String** |  | [optional] |
| **paid_at** | **Time** |  |  |
| **created_at** | **Time** |  |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::Receipt.new(
  uuid: null,
  transaction_id: null,
  invoice_number: null,
  amount: null,
  tax: null,
  currency: null,
  receipt_url: null,
  description: null,
  paid_at: null,
  created_at: null
)
```

