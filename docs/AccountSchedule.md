# PostBoost::AccountSchedule

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | ID of one of the post&#39;s accounts. Entries for accounts the post does not carry are ignored. |  |
| **date** | **Date** |  |  |
| **time** | **String** | H:i, read in the request &#x60;timezone&#x60;. Must not be in the past. |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::AccountSchedule.new(
  account_id: null,
  date: 2026-11-01,
  time: 14:30
)
```

