# PostBoost::FreeToolPlanPostingFrequencyResponseNetworksInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **network** | **String** |  | [optional] |
| **label** | **String** |  | [optional] |
| **recommended_per_week** | [**FreeToolPlanPostingFrequencyResponseNetworksInnerRecommendedPerWeek**](FreeToolPlanPostingFrequencyResponseNetworksInnerRecommendedPerWeek.md) |  | [optional] |
| **recommended_label** | **String** | The range as text, e.g. \&quot;3-5 per week\&quot; or \&quot;1+ per week\&quot;. | [optional] |
| **allocated_per_week** | **Integer** | Your posts for this network: capacity split in proportion to the range midpoints (the minimum for an open-ended range). | [optional] |
| **fit** | **String** | Where the allocation sits against the recommended range. | [optional] |
| **source_type** | **String** | measured &#x3D; a study of real posts; vendor &#x3D; a software vendor&#39;s guidance; platform &#x3D; the network&#39;s own guidance. | [optional] |
| **sources** | [**Array&lt;FreeToolPlanPostingFrequencyResponseNetworksInnerSourcesInner&gt;**](FreeToolPlanPostingFrequencyResponseNetworksInnerSourcesInner.md) |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolPlanPostingFrequencyResponseNetworksInner.new(
  network: null,
  label: null,
  recommended_per_week: null,
  recommended_label: null,
  allocated_per_week: null,
  fit: null,
  source_type: null,
  sources: null
)
```

