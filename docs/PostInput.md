# PostBoost::PostInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **versions** | [**Array&lt;PostVersion&gt;**](PostVersion.md) | At least one version with &#x60;is_original: true&#x60; is required. |  |
| **accounts** | **Array&lt;Integer&gt;** | Account IDs to publish to. | [optional] |
| **tags** | **Array&lt;Integer&gt;** | Tag IDs to attach. | [optional] |
| **date** | **Date** |  | [optional] |
| **time** | **String** |  | [optional] |
| **timezone** | **String** | Timezone &#x60;date&#x60;, &#x60;time&#x60; and &#x60;accounts_schedule&#x60; are read in. Defaults to the workspace timezone. | [optional] |
| **accounts_schedule** | [**Array&lt;AccountSchedule&gt;**](AccountSchedule.md) | Per-account departure times. When omitted on update, accounts keep their offsets from the post time. | [optional] |
| **schedule** | **Boolean** | Schedule the post for the given date/time. | [optional] |
| **schedule_now** | **Boolean** | Publish immediately. | [optional] |
| **queue** | **Boolean** | Add to the smart publishing queue. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::PostInput.new(
  versions: null,
  accounts: null,
  tags: null,
  date: 2025-06-01,
  time: 10:00,
  timezone: America/New_York,
  accounts_schedule: null,
  schedule: null,
  schedule_now: null,
  queue: null
)
```

