# PostBoost::FreeToolGenerateYoutubeTitlesResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **titles** | **Array&lt;String&gt;** | Three to five different titles, each at most 100 characters, with the main keyword early, no &#x60;&lt;&#x60; or &#x60;&gt;&#x60; and not in capitals. | [optional] |
| **credits_spent** | **Integer** | AI credits this call took from the workspace: 1, or 0 for a cached result. | [optional] |
| **cached** | **Boolean** | True when the same request was answered before (free). | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolGenerateYoutubeTitlesResponse.new(
  titles: null,
  credits_spent: null,
  cached: null
)
```

