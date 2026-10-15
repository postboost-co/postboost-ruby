# PostBoost::FreeToolGenerateHashtagsRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **topic** | **String** | What the post is about. |  |
| **niche** | **String** | Optional niche from the hashtag generator page. | [optional] |
| **network** | **String** | The network the text is written for. | [optional][default to &#39;instagram&#39;] |
| **workspace** | **String** | UUID of the workspace whose AI credits pay for the call. Default: your active workspace (a scoped API key: its own workspace). | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolGenerateHashtagsRequest.new(
  topic: null,
  niche: null,
  network: null,
  workspace: null
)
```

