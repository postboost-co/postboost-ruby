# PostBoost::ConnectChannelInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **bot_token** | **String** | Telegram only. Bot token from @BotFather. | [optional] |
| **chat** | **String** | Telegram only. Channel &#x60;@username&#x60; or numeric chat id. | [optional] |
| **webhook_url** | **String** | Discord or Slack incoming webhook URL. | [optional] |
| **name** | **String** | Slack only. Display name for the channel (Slack webhooks do not report one). | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::ConnectChannelInput.new(
  bot_token: 123456789:AAHdqTcvCH1vGWJxfSeofSAs0K5PALDsawQ,
  chat: @yourchannel,
  webhook_url: null,
  name: null
)
```

