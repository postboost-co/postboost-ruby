# PostBoost::InboxReplyDraftInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **body** | **String** | The reply text. Limit depends on the network. |  |
| **in_reply_to** | **String** | Message &#x60;id&#x60; to reply to; defaults to the latest incoming message. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::InboxReplyDraftInput.new(
  body: null,
  in_reply_to: null
)
```

