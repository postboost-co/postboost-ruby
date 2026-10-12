# PostBoost::PostingScheduleInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | 0 for the workspace schedule, or an account &#x60;id&#x60;. |  |
| **timezone** | **String** |  |  |
| **auto_tune** | **Boolean** |  | [optional] |
| **times** | [**Array&lt;PostingScheduleDay&gt;**](PostingScheduleDay.md) |  |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::PostingScheduleInput.new(
  account_id: null,
  timezone: Europe/Amsterdam,
  auto_tune: null,
  times: null
)
```

