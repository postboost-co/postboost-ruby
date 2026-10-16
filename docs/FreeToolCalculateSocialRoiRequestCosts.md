# PostBoost::FreeToolCalculateSocialRoiRequestCosts

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **ad_spend** | **Float** | Paid social ad spend. | [optional][default to 0] |
| **tools** | **Float** | Tools and software subscriptions. | [optional][default to 0] |
| **labor_hours** | **Float** | Hours spent on social media. | [optional][default to 0] |
| **hourly_rate** | **Float** | Cost of one hour of that work. | [optional][default to 0] |
| **content** | **Float** | Content production: design, video, photography, freelancers. | [optional][default to 0] |
| **other** | **Float** | Anything else. | [optional][default to 0] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolCalculateSocialRoiRequestCosts.new(
  ad_spend: null,
  tools: null,
  labor_hours: null,
  hourly_rate: null,
  content: null,
  other: null
)
```

