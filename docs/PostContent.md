# PostBoost::PostContent

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **body** | **String** | Post text/caption. For a second item on Facebook Page, Instagram or LinkedIn this is the first comment. | [optional] |
| **url** | **String** |  | [optional] |
| **media** | **Array&lt;Integer&gt;** | Array of media IDs from the media library. | [optional] |
| **video_thumbs** | **Array&lt;Object&gt;** |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::PostContent.new(
  body: null,
  url: null,
  media: null,
  video_thumbs: null
)
```

