# PostBoost::DeleteMediaBulkRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **items** | [**Array&lt;DeleteMediaBulkRequestItemsInner&gt;**](DeleteMediaBulkRequestItemsInner.md) | Array of media IDs or UUIDs to delete. |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::DeleteMediaBulkRequest.new(
  items: null
)
```

