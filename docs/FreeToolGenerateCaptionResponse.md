# PostBoost::FreeToolGenerateCaptionResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **captions** | **Array&lt;String&gt;** | Three different captions. | [optional] |
| **credits_spent** | **Integer** | AI credits this call took from the workspace: 1, or 0 for a cached result. | [optional] |
| **cached** | **Boolean** | True when the same request was answered before (free). | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolGenerateCaptionResponse.new(
  captions: null,
  credits_spent: null,
  cached: null
)
```

