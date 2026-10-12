# PostBoost::QueueSlots

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **slots** | **Array&lt;Hash&lt;String, Object&gt;&gt;** | Upcoming posting times and scheduled posts, in order. |  |
| **next_cursor** | **String** | Pass as &#x60;after&#x60; for the next page; null at the end. |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::QueueSlots.new(
  slots: null,
  next_cursor: null
)
```

