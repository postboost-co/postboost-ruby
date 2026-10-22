# PostBoost::FreeToolGenerateSocialPostsFromVideoResponseOutputs

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **x_thread** | **Array&lt;String&gt;** | The thread&#39;s posts in order, each within X&#39;s 280 weighted characters; the link is in the last one. | [optional] |
| **linkedin** | **String** | A LinkedIn caption within the network&#39;s character limit. | [optional] |
| **instagram** | **String** | A Instagram caption within the network&#39;s character limit. | [optional] |
| **facebook** | **String** | A Facebook caption within the network&#39;s character limit. | [optional] |
| **threads** | **String** | A Threads caption within the network&#39;s character limit. | [optional] |
| **bluesky** | **String** | A Bluesky caption within the network&#39;s character limit. | [optional] |
| **mastodon** | **String** | A Mastodon caption within the network&#39;s character limit. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolGenerateSocialPostsFromVideoResponseOutputs.new(
  x_thread: null,
  linkedin: null,
  instagram: null,
  facebook: null,
  threads: null,
  bluesky: null,
  mastodon: null
)
```

