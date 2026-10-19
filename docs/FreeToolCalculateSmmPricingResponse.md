# PostBoost::FreeToolCalculateSmmPricingResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **currency** | **String** |  | [optional] |
| **pricing_model** | **String** |  | [optional] |
| **posts_per_month** | **Float** | Networks × posts per week × 52 ÷ 12, 1 decimal. | [optional] |
| **hours_per_month** | **Float** | Estimated working hours a month, 1 decimal. | [optional] |
| **hourly_rate** | **Float** |  | [optional] |
| **monthly_retainer** | **Float** | Hours a month × hourly rate, whole currency units. | [optional] |
| **per_post** | **Float** | Monthly retainer ÷ posts a month, 2 decimals; null with no posts. | [optional] |
| **range** | [**FreeToolCalculateSmmPricingResponseRange**](FreeToolCalculateSmmPricingResponseRange.md) |  | [optional] |
| **line_items** | [**Array&lt;FreeToolCalculateSmmPricingResponseLineItemsInner&gt;**](FreeToolCalculateSmmPricingResponseLineItemsInner.md) | Every task with hours above 0. | [optional] |
| **assumptions** | **Array&lt;String&gt;** |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolCalculateSmmPricingResponse.new(
  currency: null,
  pricing_model: null,
  posts_per_month: null,
  hours_per_month: null,
  hourly_rate: null,
  monthly_retainer: null,
  per_post: null,
  range: null,
  line_items: null,
  assumptions: null
)
```

