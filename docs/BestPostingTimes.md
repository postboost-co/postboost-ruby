# PostBoost::BestPostingTimes

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **timezone** | **String** |  |  |
| **times** | [**Array&lt;BestPostingTimesTimesInner&gt;**](BestPostingTimesTimesInner.md) | The next recommended time per account. Accounts without enough history are left out. |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::BestPostingTimes.new(
  timezone: null,
  times: null
)
```

