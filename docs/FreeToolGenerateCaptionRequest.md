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
| **format** | **String** | caption: short captions (default). post: long-form posts of 300-600, 600-1,300 or 1,300-2,000 characters by &#x60;length&#x60;, with at most 3 hashtags; network linkedin only. | [optional][default to &#39;caption&#39;] |

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
  workspace: null,
  format: null
)
```

