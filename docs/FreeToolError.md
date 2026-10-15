# PostBoost::FreeToolError

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **message** | **String** |  |  |
| **retry_after** | **Integer** | 429 only: seconds until the limit resets. | [optional] |
| **code** | **String** | 429 of a paid AI tool: &#x60;ai_credits_exhausted&#x60;. | [optional] |
| **register_url** | **String** | 429 for guests: sign up for a token with higher limits. 401 of a paid AI tool: sign up for a token. | [optional] |
| **upgrade_url** | **String** | 429 when a token user reached the plan&#39;s daily cap, or a paid AI tool&#39;s workspace has no AI credits left. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolError.new(
  message: null,
  retry_after: null,
  code: null,
  register_url: null,
  upgrade_url: null
)
```

