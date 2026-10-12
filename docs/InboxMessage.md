# PostBoost::InboxMessage

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Message UUID. |  |
| **direction** | **String** |  |  |
| **body** | **String** |  |  |
| **author** | [**InboxMessageAuthor**](InboxMessageAuthor.md) |  | [optional] |
| **sentiment** | **String** |  | [optional] |
| **ai_label** | **String** |  | [optional] |
| **is_spam** | **Boolean** |  | [optional] |
| **created_at** | **Time** |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::InboxMessage.new(
  id: null,
  direction: null,
  body: null,
  author: null,
  sentiment: null,
  ai_label: null,
  is_spam: null,
  created_at: null
)
```

