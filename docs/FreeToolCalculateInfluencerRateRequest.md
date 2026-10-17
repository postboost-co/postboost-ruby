# PostBoost::FreeToolCalculateInfluencerRateRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **network** | **String** | LinkedIn is not offered: no primary source for its rates. |  |
| **followers** | **Integer** | Followers (subscribers on YouTube). Sets the tier. |  |
| **deliverable** | **String** | Instagram: post (default), reel, carousel. TikTok: video. X and Facebook: post. YouTube: integration (default), dedicated, short. | [optional] |
| **avg_views** | **Integer** | Expected views of the deliverable. Required on YouTube, which is priced per 1,000 views; with cpm_usd it gives your own CPM estimate on any network. | [optional] |
| **cpm_usd** | **Integer** | Your own price per 1,000 views, in whole USD, for the CPM estimate. | [optional] |
| **usage_rights_months** | **Integer** | Months the brand may reuse the content. | [optional][default to 0] |
| **exclusivity** | **Boolean** | The creator agrees not to work with competitors for the campaign. | [optional][default to false] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolCalculateInfluencerRateRequest.new(
  network: null,
  followers: null,
  deliverable: null,
  avg_views: null,
  cpm_usd: null,
  usage_rights_months: null,
  exclusivity: null
)
```

