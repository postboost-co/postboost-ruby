# PostBoost::RssFeed

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **uuid** | **String** |  |  |
| **url** | **String** |  |  |
| **name** | **String** |  |  |
| **account_ids** | **Array&lt;Integer&gt;** |  |  |
| **mode** | **String** |  |  |
| **template** | **String** |  |  |
| **max_items_per_run** | **Integer** |  |  |
| **active** | **Boolean** |  |  |
| **last_polled_at** | **Time** |  |  |
| **last_error** | **String** | Error of the last check; after 5 failures in a row the feed is checked every 6 hours. |  |
| **created_at** | **Time** |  |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::RssFeed.new(
  uuid: null,
  url: null,
  name: null,
  account_ids: null,
  mode: null,
  template: null,
  max_items_per_run: null,
  active: null,
  last_polled_at: null,
  last_error: null,
  created_at: null
)
```

