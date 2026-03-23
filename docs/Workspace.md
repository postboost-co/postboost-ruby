# PostBoost::Workspace

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **uuid** | **String** |  | [optional] |
| **name** | **String** |  | [optional] |
| **hex_color** | **String** |  | [optional] |
| **owner** | [**User**](User.md) |  | [optional] |
| **access_status** | **String** |  | [optional] |
| **created_at** | **Time** |  | [optional] |

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

