# PostBoost::FreeToolSummarizeReportResponseNetworksInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **network** | **String** |  | [optional] |
| **posts** | **Integer** |  | [optional] |
| **views** | **Integer** |  | [optional] |
| **engagements** | **Integer** |  | [optional] |
| **rate** | **Float** | Percent, 2 decimals; null without views. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolSummarizeReportResponseNetworksInner.new(
  network: null,
  posts: null,
  views: null,
  engagements: null,
  rate: null
)
```

