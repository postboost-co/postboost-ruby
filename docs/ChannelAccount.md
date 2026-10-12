# PostBoost::ChannelAccount

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** |  |  |
| **uuid** | **String** |  |  |
| **name** | **String** |  |  |
| **username** | **String** | Telegram public channel username; null for private channels, Discord and Slack. | [optional] |
| **image** | **String** |  | [optional] |
| **provider** | **String** |  |  |
| **data** | **Object** | Provider metadata (Telegram &#x60;chat_id&#x60;, Discord &#x60;channel_id&#x60;/&#x60;guild_id&#x60;, Slack &#x60;team_id&#x60;). |  |
| **authorized** | **Boolean** |  |  |
| **profile_url** | **String** |  | [optional] |
| **created_at** | **String** |  |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::ChannelAccount.new(
  id: null,
  uuid: null,
  name: Product news,
  username: null,
  image: null,
  provider: null,
  data: null,
  authorized: null,
  profile_url: null,
  created_at: null
)
```

