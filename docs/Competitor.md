# PostBoost::Competitor

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** |  |  |
| **account_id** | **Integer** |  |  |
| **username** | **String** |  |  |
| **name** | **String** |  | [optional] |
| **image** | **String** |  | [optional] |
| **followers_count** | **Integer** |  | [optional] |
| **media_count** | **Integer** |  | [optional] |
| **avg_engagement** | **Integer** | Average likes plus comments per imported post. |  |
| **last_snapshot_date** | **Date** |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::Competitor.new(
  id: null,
  account_id: null,
  username: natgeo,
  name: null,
  image: null,
  followers_count: null,
  media_count: null,
  avg_engagement: null,
  last_snapshot_date: null
)
```

