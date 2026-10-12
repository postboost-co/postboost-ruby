# PostBoost::InboxConversation

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Conversation UUID. |  |
| **provider** | **String** |  |  |
| **type** | **String** |  | [optional] |
| **status** | **String** |  |  |
| **unread** | **Boolean** |  |  |
| **sentiment** | **String** |  | [optional] |
| **ai_label** | **String** |  | [optional] |
| **is_spam** | **Boolean** |  | [optional] |
| **is_hidden** | **Boolean** |  | [optional] |
| **provider_post_id** | **String** |  | [optional] |
| **account** | [**InboxConversationAccount**](InboxConversationAccount.md) |  | [optional] |
| **author** | [**InboxMessageAuthor**](InboxMessageAuthor.md) |  | [optional] |
| **latest_message** | **Object** | Only in lists. | [optional] |
| **messages** | [**Array&lt;InboxMessage&gt;**](InboxMessage.md) | Only on &#x60;GET inbox/conversations/{conversationId}&#x60;. | [optional] |
| **last_message_at** | **Time** |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::InboxConversation.new(
  id: null,
  provider: bluesky,
  type: null,
  status: null,
  unread: null,
  sentiment: null,
  ai_label: null,
  is_spam: null,
  is_hidden: null,
  provider_post_id: null,
  account: null,
  author: null,
  latest_message: null,
  messages: null,
  last_message_at: null
)
```

