# PostBoost::Receipt

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **uuid** | **String** |  | [optional] |
| **transaction_id** | **String** |  | [optional] |
| **invoice_number** | **String** |  | [optional] |
| **amount** | **Float** |  | [optional] |
| **tax** | **Float** |  | [optional] |
| **currency** | **String** |  | [optional] |
| **receipt_url** | **String** |  | [optional] |
| **description** | **String** |  | [optional] |
| **paid_at** | **Time** |  | [optional] |
| **created_at** | **Time** |  | [optional] |

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

