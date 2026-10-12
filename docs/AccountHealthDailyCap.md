# PostBoost::AccountHealthDailyCap

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **limit** | **Integer** | Posts allowed per UTC day for this network. |  |
| **used_today** | **Integer** | Scheduled, awaiting-approval and published posts counted for today (UTC). |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::AccountHealthDailyCap.new(
  limit: null,
  used_today: null
)
```

