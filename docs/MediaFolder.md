# PostBoost::MediaFolder

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **uuid** | **String** |  |  |
| **name** | **String** |  |  |
| **parent** | **String** | UUID of the parent folder; null for a top-level folder. |  |
| **media_count** | **Integer** | Media filed anywhere below the folder, including its sub-folders. |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::MediaFolder.new(
  uuid: null,
  name: Campaign assets,
  parent: null,
  media_count: null
)
```

