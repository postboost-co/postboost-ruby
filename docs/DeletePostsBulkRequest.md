# PostBoost::DeletePostsBulkRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **posts** | **Array&lt;String&gt;** | Array of post UUIDs to delete. |  |
| **trash** | **Boolean** | Move to trash instead of permanent delete. | [optional][default to false] |
| **delete_mode** | [**DeleteMode**](DeleteMode.md) |  | [optional][default to &#39;app_only&#39;] |

## Example

```ruby
require 'postboost'

instance = PostBoost::DeletePostsBulkRequest.new(
  posts: null,
  trash: null,
  delete_mode: null
)
```

