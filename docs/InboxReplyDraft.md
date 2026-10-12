# PostBoost::InboxReplyDraft

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Draft UUID. |  |
| **status** | **String** |  |  |
| **body** | **String** |  |  |
| **source** | **String** |  |  |
| **conversation_id** | **String** |  | [optional] |
| **provider** | **String** |  | [optional] |
| **in_reply_to** | **Object** | The incoming message this replies to (same shape as &#x60;InboxMessage&#x60;). | [optional] |
| **created_by** | **String** | Name of the user whose API key wrote the draft. | [optional] |
| **reviewed_by** | **String** |  | [optional] |
| **reviewed_at** | **Time** |  | [optional] |
| **sent_message_id** | **String** | The sent reply&#39;s message UUID, once sent. | [optional] |
| **error** | **String** | Why sending failed. | [optional] |
| **created_at** | **Time** |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::InboxReplyDraft.new(
  id: null,
  status: null,
  body: null,
  source: null,
  conversation_id: null,
  provider: null,
  in_reply_to: null,
  created_by: null,
  reviewed_by: null,
  reviewed_at: null,
  sent_message_id: null,
  error: null,
  created_at: null
)
```

