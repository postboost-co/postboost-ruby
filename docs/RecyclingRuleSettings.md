# PostBoost::RecyclingRuleSettings

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **interval_days** | **Integer** | Days between copies. |  |
| **max_runs** | **Integer** | Copies to create before the rule stops; null &#x3D; no limit. | [optional] |
| **placement** | **String** | &#x60;queue&#x60;: each account&#39;s next free queue slot (skipped when the queue is full for 14 days). &#x60;same_time&#x60;: the source post&#39;s time of day. &#x60;draft&#x60;: a draft only. | [optional][default to &#39;queue&#39;] |
| **account_ids** | **Array&lt;Integer&gt;** | Accounts for the copies; default the source post&#39;s accounts. For a tag pool, limits each picked post&#39;s accounts. | [optional] |
| **start_at** | **Time** | First run; default one interval from now. | [optional] |
| **active** | **Boolean** |  | [optional][default to true] |

## Example

```ruby
require 'postboost'

instance = PostBoost::RecyclingRuleSettings.new(
  interval_days: null,
  max_runs: null,
  placement: null,
  account_ids: null,
  start_at: null,
  active: null
)
```

