# PostBoost::ReportExport

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **uuid** | **String** |  |  |
| **format** | **String** |  |  |
| **dataset** | **String** |  |  |
| **period** | **String** |  |  |
| **date_from** | **Date** |  |  |
| **date_to** | **Date** |  |  |
| **account_ids** | **Array&lt;Integer&gt;** |  |  |
| **status** | **String** |  |  |
| **error** | **String** |  |  |
| **bytes** | **Integer** |  |  |
| **download_url** | **String** | Authenticated download URL while the file is available. |  |
| **created_at** | **Time** |  |  |
| **expires_at** | **Time** |  |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::ReportExport.new(
  uuid: null,
  format: null,
  dataset: null,
  period: null,
  date_from: null,
  date_to: null,
  account_ids: null,
  status: null,
  error: null,
  bytes: null,
  download_url: null,
  created_at: null,
  expires_at: null
)
```

