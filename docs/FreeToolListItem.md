# PostBoost::FreeToolListItem

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **slug** | **String** |  |  |
| **name** | **String** |  |  |
| **operation_id** | **String** |  |  |
| **kind** | **String** |  |  |
| **limits** | **String** | Limit profile: std, fetch or ai. |  |
| **page_url** | **String** |  |  |
| **docs_url** | **String** |  |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolListItem.new(
  slug: x-thread-maker,
  name: null,
  operation_id: splitThread,
  kind: null,
  limits: null,
  page_url: null,
  docs_url: null
)
```

