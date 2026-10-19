# PostBoost::FreeToolSummarizeReportRequestRowsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **date** | **String** | Publish date; only a leading YYYY-MM-DD is read. | [optional] |
| **network** | **String** |  | [optional] |
| **text** | **String** | The post text, a full caption is fine; the top posts show its first 80 characters. | [optional] |
| **views** | **Integer** |  | [optional] |
| **likes** | **Integer** |  | [optional] |
| **comments** | **Integer** |  | [optional] |
| **shares** | **Integer** |  | [optional] |
| **clicks** | **Integer** |  | [optional] |
| **engagements** | **Integer** |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolSummarizeReportRequestRowsInner.new(
  date: null,
  network: null,
  text: null,
  views: null,
  likes: null,
  comments: null,
  shares: null,
  clicks: null,
  engagements: null
)
```

