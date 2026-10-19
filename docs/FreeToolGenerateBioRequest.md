# PostBoost::FreeToolGenerateBioRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **text** | **String** | What you or your brand do, and for whom. |  |
| **tone** | **String** |  | [optional][default to &#39;friendly&#39;] |
| **emoji** | **Boolean** | Use one or two fitting emoji. | [optional][default to true] |
| **cta** | **Boolean** | End with a short call to action, such as the link in bio. | [optional][default to true] |
| **network** | **String** | The network the bio is written for (Instagram for now). | [optional][default to &#39;instagram&#39;] |
| **workspace** | **String** | UUID of the workspace whose AI credits pay for the call. Default: your active workspace (a scoped API key: its own workspace). | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolGenerateBioRequest.new(
  text: null,
  tone: null,
  emoji: null,
  cta: null,
  network: null,
  workspace: null
)
```

