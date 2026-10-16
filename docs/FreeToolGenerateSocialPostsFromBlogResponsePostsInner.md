# PostBoost::FreeToolGenerateSocialPostsFromBlogResponsePostsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **platform** | **String** |  | [optional] |
| **text** | **String** | The post, cut at a sentence end when the model ran over the limit. | [optional] |
| **hashtags** | **Array&lt;String&gt;** | Hashtags in the text, with #. | [optional] |
| **characters** | **Integer** | Length as the network counts it (X weighs links as 23, YouTube counts bytes). | [optional] |
| **limit** | **Integer** | The network&#39;s text limit. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolGenerateSocialPostsFromBlogResponsePostsInner.new(
  platform: null,
  text: null,
  hashtags: null,
  characters: null,
  limit: null
)
```

