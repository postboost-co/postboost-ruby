# PostBoost::FreeToolCheckReadabilityRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **text** | **String** | The post text. |  |
| **language** | **String** | Language code. Only English (&#x60;en&#x60;) is scored; other languages return &#x60;supported: false&#x60; and no scores. | [optional][default to &#39;en&#39;] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolCheckReadabilityRequest.new(
  text: null,
  language: null
)
```

