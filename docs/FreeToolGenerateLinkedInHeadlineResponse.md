# PostBoost::FreeToolGenerateLinkedInHeadlineResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **headlines** | **Array&lt;String&gt;** | Three to five different headlines, each at most 220 characters as the character counter counts them. | [optional] |
| **credits_spent** | **Integer** | AI credits this call took from the workspace: 1, or 0 for a cached result. | [optional] |
| **cached** | **Boolean** | True when the same request was answered before (free). | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolGenerateLinkedInHeadlineResponse.new(
  headlines: null,
  credits_spent: null,
  cached: null
)
```

