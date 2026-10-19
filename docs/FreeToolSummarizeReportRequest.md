# PostBoost::FreeToolSummarizeReportRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **rows** | [**Array&lt;FreeToolSummarizeReportRequestRowsInner&gt;**](FreeToolSummarizeReportRequestRowsInner.md) | One object per post, already mapped to these fields. Leave out a count the export does not have. |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolSummarizeReportRequest.new(
  rows: null
)
```

