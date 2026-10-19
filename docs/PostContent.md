# PostBoost::PostContent

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **body** | **String** | Post text/caption. For a second item on Facebook Page, Instagram or LinkedIn this is the first comment. | [optional] |
| **url** | **String** | Link shown as a preview card on LinkedIn, Bluesky and Facebook Pages (Facebook builds the card from the page&#39;s own Open Graph tags). If omitted and the item has no media, the first link in &#x60;body&#x60; is used. | [optional] |
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

