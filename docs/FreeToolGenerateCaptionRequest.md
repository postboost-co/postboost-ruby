# PostBoost::FreeToolGenerateCaptionRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **text** | **String** | What the post is about. |  |
| **tone** | **String** |  | [optional][default to &#39;friendly&#39;] |
| **length** | **String** | short: 10-20 words, medium: 25-40, long: 45-60. | [optional][default to &#39;medium&#39;] |
| **emoji** | **Boolean** | Use a few fitting emoji. | [optional][default to true] |
| **hashtags** | **Boolean** | End each caption with 3-5 relevant hashtags. | [optional][default to false] |
| **network** | **String** | The network the text is written for. | [optional][default to &#39;instagram&#39;] |
| **workspace** | **String** | UUID of the workspace whose AI credits pay for the call. Default: your active workspace (a scoped API key: its own workspace). | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolGenerateCaptionRequest.new(
  text: null,
  tone: null,
  length: null,
  emoji: null,
  hashtags: null,
  network: null,
  workspace: null
)
```

