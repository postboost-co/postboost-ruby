# PostBoost::AIUsageText

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **used** | **Integer** | &#x60;null&#x60; when the workspace has no text credit limit. |  |
| **limit** | **Integer** |  |  |
| **remaining** | **Integer** |  |  |
| **cycle_started_at** | **Time** |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::AIUsageText.new(
  used: null,
  limit: null,
  remaining: null,
  cycle_started_at: null
)
```

