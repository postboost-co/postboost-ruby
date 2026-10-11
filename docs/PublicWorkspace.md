# PostBoost::PublicWorkspace

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** |  |  |
| **uuid** | **String** |  |  |
| **name** | **String** |  |  |
| **pivot** | [**PublicWorkspacePivot**](PublicWorkspacePivot.md) |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::PublicWorkspace.new(
  id: null,
  uuid: null,
  name: Acme Marketing,
  pivot: null
)
```

