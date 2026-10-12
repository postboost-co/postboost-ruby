# PostBoost::WorkspaceAgent

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **uuid** | **String** |  |  |
| **type** | **String** |  |  |
| **name** | **String** |  |  |
| **enabled** | **Boolean** |  |  |
| **schedule** | **String** |  |  |
| **settings** | [**WorkspaceAgentSettings**](WorkspaceAgentSettings.md) |  |  |
| **last_run_at** | **Time** |  |  |
| **next_run_at** | **Time** |  |  |
| **created_at** | **Time** |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::WorkspaceAgent.new(
  uuid: null,
  type: null,
  name: null,
  enabled: null,
  schedule: null,
  settings: null,
  last_run_at: null,
  next_run_at: null,
  created_at: null
)
```

