# PostBoost::FreeToolGenerateHooksRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **topic** | **String** | What the post is about. |  |
| **tone** | **String** | Tone of the hooks, as on the caption generator. | [optional][default to &#39;friendly&#39;] |
| **count** | **Integer** | How many hooks to write. | [optional][default to 5] |
| **network** | **String** | The network the text is written for. | [optional][default to &#39;instagram&#39;] |
| **workspace** | **String** | UUID of the workspace whose AI credits pay for the call. Default: your active workspace (a scoped API key: its own workspace). | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolGenerateHooksRequest.new(
  topic: null,
  tone: null,
  count: null,
  network: null,
  workspace: null
)
```

