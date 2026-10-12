# PostBoost::PostingSchedule

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The account asked for; 0 for the workspace schedule. |  |
| **source_account_id** | **Integer** | Whose schedule applies; 0 when the workspace schedule applies. |  |
| **inherited** | **Boolean** | True when the account follows the workspace schedule. |  |
| **timezone** | **String** |  |  |
| **auto_tune** | **Boolean** | Adjust times automatically from engagement data. |  |
| **times** | [**Array&lt;PostingScheduleDay&gt;**](PostingScheduleDay.md) |  |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::PostingSchedule.new(
  account_id: null,
  source_account_id: null,
  inherited: null,
  timezone: Europe/Amsterdam,
  auto_tune: null,
  times: null
)
```

