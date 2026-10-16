# PostBoost::FreeToolCalculateXApiCostRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **posts** | **Integer** | Posts created per month, with or without a link. | [optional][default to 0] |
| **link_share** | **Integer** | Percent of those posts that contain a URL (billed at the link-post price). | [optional][default to 0] |
| **replies** | **Integer** | Summoned replies per month. | [optional][default to 0] |
| **post_reads** | **Integer** | Posts read per month. | [optional][default to 0] |
| **user_reads** | **Integer** | Users read per month. | [optional][default to 0] |
| **owned_reads** | **Integer** | Owned resources read per month (your own posts, followers and so on). | [optional][default to 0] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolCalculateXApiCostRequest.new(
  posts: null,
  link_share: null,
  replies: null,
  post_reads: null,
  user_reads: null,
  owned_reads: null
)
```

