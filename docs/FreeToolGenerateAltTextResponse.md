# PostBoost::FreeToolGenerateAltTextResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **alt_text** | **String** | The alt text, within the chosen length. | [optional] |
| **short_alt_text** | **String** | A shorter alternative. | [optional] |
| **credits_spent** | **Integer** | AI credits this call took from the workspace: 1, or 0 for a cached result. | [optional] |
| **cached** | **Boolean** | True when the same request was answered before (free). | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolGenerateAltTextResponse.new(
  alt_text: null,
  short_alt_text: null,
  credits_spent: null,
  cached: null
)
```

