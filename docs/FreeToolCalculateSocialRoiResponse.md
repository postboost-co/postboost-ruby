# PostBoost::FreeToolCalculateSocialRoiResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **period** | **String** |  | [optional] |
| **revenue** | **Float** |  | [optional] |
| **total_cost** | **Float** | Sum of every cost, labor &#x3D; hours × hourly rate. 2 decimals. | [optional] |
| **net_return** | **Float** | Revenue minus total cost. 2 decimals. | [optional] |
| **roi_percent** | **Float** | (revenue − total cost) ÷ total cost × 100, 1 decimal; null when the total cost is 0. | [optional] |
| **cost_breakdown** | [**Array&lt;FreeToolCalculateSocialRoiResponseCostBreakdownInner&gt;**](FreeToolCalculateSocialRoiResponseCostBreakdownInner.md) | Every cost above 0, with its share of the total cost (percent, 1 decimal). | [optional] |
| **warnings** | **Array&lt;String&gt;** |  | [optional] |
| **formula** | **String** |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolCalculateSocialRoiResponse.new(
  period: null,
  revenue: null,
  total_cost: null,
  net_return: null,
  roi_percent: null,
  cost_breakdown: null,
  warnings: null,
  formula: null
)
```

