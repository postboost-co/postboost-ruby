# PostBoost::FreeToolScoreSocialAuditResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **score** | **Integer** | Overall score: all points over the maximum, as 0-100 rounded half up. | [optional] |
| **networks** | [**Array&lt;FreeToolScoreSocialAuditResponseNetworksInner&gt;**](FreeToolScoreSocialAuditResponseNetworksInner.md) | One row per audited network, in a fixed network order. | [optional] |
| **top_fixes** | [**Array&lt;FreeToolScoreSocialAuditResponseTopFixesInner&gt;**](FreeToolScoreSocialAuditResponseTopFixesInner.md) | Up to 3 questions with the fewest points over all audited networks (ties: checklist order); only questions answered below yes somewhere. | [optional] |
| **report_markdown** | **String** | The scorecard as a Markdown report: overall score, top fixes and every answer per network. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolScoreSocialAuditResponse.new(
  score: null,
  networks: null,
  top_fixes: null,
  report_markdown: null
)
```

