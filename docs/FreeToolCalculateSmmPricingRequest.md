# PostBoost::FreeToolCalculateSmmPricingRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **networks** | **Integer** | Number of social networks managed. |  |
| **posts_per_week** | **Integer** | Posts per week on each network. |  |
| **content_type** | **String** | What goes into a post. Assumed minutes per post: copy 30, copy_design 60, copy_design_video 120. | [optional][default to &#39;copy_design&#39;] |
| **community_hours_per_week** | **Float** | Community management (replies, comments, DMs), hours per week. | [optional][default to 0] |
| **reporting_hours_per_month** | **Float** | Reporting, hours per month. | [optional][default to 0] |
| **ad_hours_per_month** | **Float** | Paid social ad management, hours per month. | [optional][default to 0] |
| **hourly_rate** | **Float** | Your hourly rate. The default 50 is a round placeholder, not a market rate. | [optional][default to 50] |
| **currency** | **String** | Currency for formatting only; nothing is converted. | [optional][default to &#39;USD&#39;] |
| **pricing_model** | **String** | Which price leads the quote: hourly, monthly retainer or per post. | [optional][default to &#39;retainer&#39;] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolCalculateSmmPricingRequest.new(
  networks: null,
  posts_per_week: null,
  content_type: null,
  community_hours_per_week: null,
  reporting_hours_per_month: null,
  ad_hours_per_month: null,
  hourly_rate: null,
  currency: null,
  pricing_model: null
)
```

