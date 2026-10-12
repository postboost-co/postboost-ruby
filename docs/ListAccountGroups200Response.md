# PostBoost::ListAccountGroups200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **links** | [**PaginationMetaLinks**](PaginationMetaLinks.md) |  | [optional] |
| **meta** | [**PaginationMetaMeta**](PaginationMetaMeta.md) |  | [optional] |
| **data** | [**Array&lt;AccountGroup&gt;**](AccountGroup.md) |  |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::ListAccountGroups200Response.new(
  links: null,
  meta: null,
  data: null
)
```

