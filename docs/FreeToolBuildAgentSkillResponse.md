# PostBoost::FreeToolBuildAgentSkillResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **format** | **String** |  | [optional] |
| **filename** | **String** |  | [optional] |
| **content** | **String** | The file, in Markdown. | [optional] |
| **install** | **Array&lt;String&gt;** | Where to put the file. | [optional] |
| **tools_used** | **Array&lt;String&gt;** | The connector tool names the content names, in first-appearance order; empty with api_token. | [optional] |
| **lines** | **Integer** |  | [optional] |
| **warnings** | [**Array&lt;FreeToolCheckPostResponseNetworksInnerErrorsInner&gt;**](FreeToolCheckPostResponseNetworksInnerErrorsInner.md) | Codes: name_normalized, task_limited_by_autonomy, autonomy_high, too_long. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolBuildAgentSkillResponse.new(
  format: null,
  filename: null,
  content: null,
  install: null,
  tools_used: null,
  lines: null,
  warnings: null
)
```

