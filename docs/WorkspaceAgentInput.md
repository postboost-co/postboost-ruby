# PostBoost::WorkspaceAgentInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  |  |
| **name** | **String** |  | [optional] |
| **enabled** | **Boolean** |  | [optional][default to true] |
| **schedule** | **String** |  | [optional][default to &#39;hourly&#39;] |
| **settings** | [**WorkspaceAgentSettings**](WorkspaceAgentSettings.md) |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::WorkspaceAgentInput.new(
  type: null,
  name: null,
  enabled: null,
  schedule: null,
  settings: null
)
```

