# PostBoost::WorkspaceInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  |  |
| **hex_color** | **String** | Ignored since v2.0; kept for backward compatibility | [optional] |
| **owner_id** | **Integer** |  | [optional] |
| **access_status** | **String** |  |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::WorkspaceInput.new(
  name: null,
  hex_color: #1d4ed8,
  owner_id: null,
  access_status: null
)
```

