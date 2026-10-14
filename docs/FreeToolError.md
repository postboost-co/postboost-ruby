# PostBoost::FreeToolError

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **message** | **String** |  |  |
| **retry_after** | **Integer** | 429 only: seconds until the limit resets. | [optional] |
| **register_url** | **String** | 429 for guests: sign up for a token with higher limits. | [optional] |
| **upgrade_url** | **String** | 429 when a token user reached the plan&#39;s daily cap. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolError.new(
  message: null,
  retry_after: null,
  register_url: null,
  upgrade_url: null
)
```

