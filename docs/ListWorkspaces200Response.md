# PostBoost::ListWorkspaces200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **links** | [**PaginationMetaLinks**](PaginationMetaLinks.md) |  | [optional] |
| **meta** | [**PaginationMetaMeta**](PaginationMetaMeta.md) |  | [optional] |
| **data** | [**Array&lt;Workspace&gt;**](Workspace.md) |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::ListWorkspaces200Response.new(
  links: null,
  meta: null,
  data: null
)
```

