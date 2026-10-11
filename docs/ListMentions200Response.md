# PostBoost::ListMentions200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **links** | [**PaginationMetaLinks**](PaginationMetaLinks.md) |  | [optional] |
| **meta** | [**PaginationMetaMeta**](PaginationMetaMeta.md) |  | [optional] |
| **data** | [**Array&lt;Mention&gt;**](Mention.md) |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::ListMentions200Response.new(
  links: null,
  meta: null,
  data: null
)
```

