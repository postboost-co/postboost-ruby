# PostBoost::FreeToolCalculateEngagementRateRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **likes** | **Integer** |  | [optional][default to 0] |
| **comments** | **Integer** |  | [optional][default to 0] |
| **shares** | **Integer** |  | [optional][default to 0] |
| **saves** | **Integer** |  | [optional][default to 0] |
| **clicks** | **Integer** |  | [optional][default to 0] |
| **method** | **String** | What to divide by. | [optional][default to &#39;followers&#39;] |
| **base** | **Integer** | Followers, or the total reach or impressions of the posts. |  |
| **posts** | **Integer** | Number of posts the engagements come from. | [optional][default to 1] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolCalculateEngagementRateRequest.new(
  likes: null,
  comments: null,
  shares: null,
  saves: null,
  clicks: null,
  method: null,
  base: null,
  posts: null
)
```

