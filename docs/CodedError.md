# PostBoost::CodedError

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **message** | **String** |  |  |
| **code** | **String** | Machine-readable reason, e.g. &#x60;ai_credits_exhausted&#x60;, &#x60;image_credits_exhausted&#x60;, &#x60;not_enough_posts&#x60;. | [optional] |
| **errors** | **Hash&lt;String, Object&gt;** |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::CodedError.new(
  message: null,
  code: null,
  errors: null
)
```

