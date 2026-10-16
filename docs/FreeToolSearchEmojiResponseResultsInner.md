# PostBoost::FreeToolSearchEmojiResponseResultsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **emoji** | **String** |  | [optional] |
| **name** | **String** | Unicode name (emoji-test.txt). | [optional] |
| **keywords** | **Array&lt;String&gt;** | CLDR English keywords. | [optional] |
| **category** | **String** |  | [optional] |
| **unicode_version** | **String** | Emoji version the emoji was added in (emoji-test.txt, e.g. 0.6 &#x3D; Unicode 6.0, 15.1). | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolSearchEmojiResponseResultsInner.new(
  emoji: null,
  name: null,
  keywords: null,
  category: null,
  unicode_version: null
)
```

