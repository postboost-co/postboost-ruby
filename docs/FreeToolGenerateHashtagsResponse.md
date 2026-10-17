# PostBoost::FreeToolGenerateHashtagsResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **hashtags** | **Array&lt;String&gt;** | 5 to 10 hashtags (3 to 6 with network tiktok), best first. | [optional] |
| **credits_spent** | **Integer** | AI credits this call took from the workspace: 1, or 0 for a cached result. | [optional] |
| **cached** | **Boolean** | True when the same request was answered before (free). | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolGenerateHashtagsResponse.new(
  hashtags: null,
  credits_spent: null,
  cached: null
)
```

