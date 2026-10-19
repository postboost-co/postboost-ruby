# PostBoost::FreeToolGenerateYoutubeDescriptionResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **descriptions** | **Array&lt;String&gt;** | Two or three different descriptions, each under 5,000 UTF-8 bytes (YouTube&#39;s limit) and without &#x60;&lt;&#x60; or &#x60;&gt;&#x60;. Links are &#x60;[link]&#x60; placeholders. | [optional] |
| **credits_spent** | **Integer** | AI credits this call took from the workspace: 1, or 0 for a cached result. | [optional] |
| **cached** | **Boolean** | True when the same request was answered before (free). | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolGenerateYoutubeDescriptionResponse.new(
  descriptions: null,
  credits_spent: null,
  cached: null
)
```

