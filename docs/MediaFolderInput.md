# PostBoost::MediaFolderInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | Folder name; must be unique among its siblings (case-insensitive). | [optional] |
| **parent** | **String** | UUID of the parent folder, or null for the top level. Folders nest to a limited depth. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::MediaFolderInput.new(
  name: null,
  parent: null
)
```

