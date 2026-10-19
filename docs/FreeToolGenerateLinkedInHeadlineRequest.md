# PostBoost::FreeToolGenerateLinkedInHeadlineRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **role** | **String** | Your role or what you do. |  |
| **skills** | **String** | Your skills and the value you bring. |  |
| **audience** | **String** | Who you help (optional). | [optional][default to &#39;&#39;] |
| **tone** | **String** |  | [optional][default to &#39;professional&#39;] |
| **workspace** | **String** | UUID of the workspace whose AI credits pay for the call. Default: your active workspace (a scoped API key: its own workspace). | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolGenerateLinkedInHeadlineRequest.new(
  role: null,
  skills: null,
  audience: null,
  tone: null,
  workspace: null
)
```

