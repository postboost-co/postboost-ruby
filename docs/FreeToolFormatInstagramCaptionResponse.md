# PostBoost::FreeToolFormatInstagramCaptionResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **text** | **String** | The caption with spacer lines, ready to paste into Instagram. | [optional] |
| **count** | **Integer** | Characters, counted like the PostBoost composer counts an Instagram caption. | [optional] |
| **limit** | **Integer** | Instagram caption limit. | [optional] |
| **over** | **Boolean** |  | [optional] |
| **hashtags** | **Integer** | Hashtags in the caption. | [optional] |
| **max_hashtags** | **Integer** | Hashtags PostBoost allows per Instagram post. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolFormatInstagramCaptionResponse.new(
  text: null,
  count: null,
  limit: null,
  over: null,
  hashtags: null,
  max_hashtags: null
)
```

