# PostBoost::FreeToolCalculateSocialRoiRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **revenue** | **Float** | Revenue attributed to social media in the period, in USD. |  |
| **costs** | [**FreeToolCalculateSocialRoiRequestCosts**](FreeToolCalculateSocialRoiRequestCosts.md) |  | [optional] |
| **period** | **String** | Optional label for the period, e.g. \&quot;Q3 2026\&quot;. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolCalculateSocialRoiRequest.new(
  revenue: null,
  costs: null,
  period: null
)
```

