# PostBoost::ReportExportInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **format** | **String** |  |  |
| **dataset** | **String** | CSV rows; default &#x60;posts&#x60;. Ignored for PDF. | [optional] |
| **period** | **String** | Default &#x60;last_month&#x60;. Ignored when &#x60;date_from&#x60; and &#x60;date_to&#x60; are sent. | [optional] |
| **date_from** | **Date** |  | [optional] |
| **date_to** | **Date** | At most 366 days after &#x60;date_from&#x60;. | [optional] |
| **account_ids** | **Array&lt;Integer&gt;** | Limit the report to these accounts; default all. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::ReportExportInput.new(
  format: null,
  dataset: null,
  period: null,
  date_from: null,
  date_to: null,
  account_ids: null
)
```

