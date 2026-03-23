# PostBoost::ListPosts200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **links** | [**PaginationMetaLinks**](PaginationMetaLinks.md) |  | [optional] |
| **meta** | [**PaginationMetaMeta**](PaginationMetaMeta.md) |  | [optional] |
| **data** | [**Array&lt;Post&gt;**](Post.md) |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::ListPosts200Response.new(
  links: null,
  meta: null,
  data: null
)
```

