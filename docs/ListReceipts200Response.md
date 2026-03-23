# PostBoost::ListReceipts200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **links** | [**PaginationMetaLinks**](PaginationMetaLinks.md) |  | [optional] |
| **meta** | [**PaginationMetaMeta**](PaginationMetaMeta.md) |  | [optional] |
| **data** | [**Array&lt;Receipt&gt;**](Receipt.md) |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::ListReceipts200Response.new(
  links: null,
  meta: null,
  data: null
)
```

