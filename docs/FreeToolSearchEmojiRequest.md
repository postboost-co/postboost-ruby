# PostBoost::FreeToolSearchEmojiRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **query** | **String** | Words to look for in the emoji name and keywords, e.g. &#x60;fire&#x60; or &#x60;party&#x60;. Empty lists the category in Unicode order. | [optional][default to &#39;&#39;] |
| **category** | **String** | Only emoji of this Unicode category. | [optional] |
| **limit** | **Integer** |  | [optional][default to 30] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolSearchEmojiRequest.new(
  query: null,
  category: null,
  limit: null
)
```

