# PostBoost::ListInboxReplyDrafts200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **links** | [**PaginationMetaLinks**](PaginationMetaLinks.md) |  | [optional] |
| **meta** | [**PaginationMetaMeta**](PaginationMetaMeta.md) |  | [optional] |
| **data** | [**Array&lt;InboxReplyDraft&gt;**](InboxReplyDraft.md) |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::ListInboxReplyDrafts200Response.new(
  links: null,
  meta: null,
  data: null
)
```

