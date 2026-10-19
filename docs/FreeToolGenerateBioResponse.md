# PostBoost::FreeToolGenerateBioResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **bios** | **Array&lt;String&gt;** | Three to five different bios, each at most 150 characters as the character counter counts them (most emoji count as 2). | [optional] |
| **credits_spent** | **Integer** | AI credits this call took from the workspace: 1, or 0 for a cached result. | [optional] |
| **cached** | **Boolean** | True when the same request was answered before (free). | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolGenerateBioResponse.new(
  bios: null,
  credits_spent: null,
  cached: null
)
```

