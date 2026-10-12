# PostBoost::PollRssFeed200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **created** | **Integer** | Posts created from new items. |  |
| **skipped** | **Integer** | New items refused by a guardrail. |  |
| **data** | [**RssFeed**](RssFeed.md) |  |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::PollRssFeed200Response.new(
  created: null,
  skipped: null,
  data: null
)
```

