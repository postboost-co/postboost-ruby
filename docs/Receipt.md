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
| **paid_at** | **String** | Display date in the configured timezone, &#x60;M j, Y&#x60; (not RFC 3339). |  |
| **created_at** | **String** | Display date in the configured timezone, &#x60;M j, Y&#x60; (not RFC 3339). |  |

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
  paid_at: Oct 16, 2026,
  created_at: Oct 16, 2026
)
```

