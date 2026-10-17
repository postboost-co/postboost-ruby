# PostBoost::FreeToolCalculateInfluencerRateResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **tier** | **String** |  | [optional] |
| **tier_label** | **String** |  | [optional] |
| **deliverable** | **String** |  | [optional] |
| **guide_low** | **Integer** | USD, low end of the vendor price-guide range after the adjustments. | [optional] |
| **guide_high** | **Integer** | USD, high end; null when the guide is open-ended (e.g. 10,000+). | [optional] |
| **guide_source** | [**FreeToolCalculateInfluencerRateResponseGuideSource**](FreeToolCalculateInfluencerRateResponseGuideSource.md) |  | [optional] |
| **marketplace_median** | **Integer** | USD, the measured median paid deliverable for this tier, all networks, before adjustments. | [optional] |
| **marketplace_note** | **String** |  | [optional] |
| **marketplace_source** | [**FreeToolCalculateInfluencerRateResponseGuideSource**](FreeToolCalculateInfluencerRateResponseGuideSource.md) |  | [optional] |
| **cpm_estimate** | **Integer** | USD, avg_views / 1,000 × cpm_usd (half up); null without both. | [optional] |
| **multipliers** | [**Array&lt;FreeToolCalculateInfluencerRateResponseMultipliersInner&gt;**](FreeToolCalculateInfluencerRateResponseMultipliersInner.md) | Every adjustment applied, as a percent of the base price. | [optional] |
| **method** | **String** |  | [optional] |
| **warnings** | **Array&lt;String&gt;** |  | [optional] |
| **currency** | **String** |  | [optional] |
| **last_verified** | **Date** |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolCalculateInfluencerRateResponse.new(
  tier: null,
  tier_label: null,
  deliverable: null,
  guide_low: null,
  guide_high: null,
  guide_source: null,
  marketplace_median: null,
  marketplace_note: null,
  marketplace_source: null,
  cpm_estimate: null,
  multipliers: null,
  method: null,
  warnings: null,
  currency: null,
  last_verified: null
)
```

