# PostBoost::FreeToolGetVideoSpecsResponseSpecsInnerLimits

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **min_seconds** | **Float** | Shortest length. Null when the source states no figure. | [optional] |
| **max_seconds** | **Float** | Longest length. Null when the source states no figure. | [optional] |
| **warn_over_seconds** | **Float** | Longer videos need a check (account type, reach), see &#x60;length&#x60;. Null when the source states no figure. | [optional] |
| **min_ratio** | **Float** | Narrowest width / height. Null when the source states no figure. | [optional] |
| **max_ratio** | **Float** | Widest width / height. Null when the source states no figure. | [optional] |
| **recommended_ratio** | **String** | Recommended ratio, e.g. &#x60;9:16&#x60;. | [optional] |
| **max_mb** | **Float** | Largest file in MB. Null when the source states no figure. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolGetVideoSpecsResponseSpecsInnerLimits.new(
  min_seconds: null,
  max_seconds: null,
  warn_over_seconds: null,
  min_ratio: null,
  max_ratio: null,
  recommended_ratio: null,
  max_mb: null
)
```

