# PostBoost::AICredits

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **available** | **Boolean** | Whether the workspace can spend AI credits now. Always true when no balance is tracked. |  |
| **balance** | **Float** | Remaining credit balance (2 decimals), or null when no balance is tracked. |  |
| **low** | **Boolean** | True when the balance is above 0 and at most 10. |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::AICredits.new(
  available: null,
  balance: null,
  low: null
)
```

