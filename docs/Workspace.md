# PostBoost::Workspace

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **uuid** | **String** |  |  |
| **name** | **String** |  |  |
| **hex_color** | **String** |  |  |
| **owner** | [**User**](User.md) |  | [optional] |
| **access_status** | **String** |  |  |
| **created_at** | **Time** |  |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::Workspace.new(
  uuid: null,
  name: null,
  hex_color: null,
  owner: null,
  access_status: null,
  created_at: null
)
```

