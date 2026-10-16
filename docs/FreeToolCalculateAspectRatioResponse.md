# PostBoost::FreeToolCalculateAspectRatioResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **ratio** | **String** | Simplified ratio, e.g. &#x60;4:5&#x60;. Decimal ratios stay as given. | [optional] |
| **decimal** | **Float** | Width divided by height, 4 decimals. | [optional] |
| **width** | **Integer** |  | [optional] |
| **height** | **Integer** |  | [optional] |
| **rounding** | [**FreeToolCalculateAspectRatioResponseRounding**](FreeToolCalculateAspectRatioResponseRounding.md) |  | [optional] |
| **orientation** | **String** |  | [optional] |
| **matches** | [**Array&lt;FreeToolCalculateAspectRatioResponseMatchesInner&gt;**](FreeToolCalculateAspectRatioResponseMatchesInner.md) | Social media image presets with the same ratio, else the nearest. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolCalculateAspectRatioResponse.new(
  ratio: null,
  decimal: null,
  width: null,
  height: null,
  rounding: null,
  orientation: null,
  matches: null
)
```

