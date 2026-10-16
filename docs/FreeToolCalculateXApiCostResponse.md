# PostBoost::FreeToolCalculateXApiCostResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **line_items** | [**Array&lt;FreeToolCalculateXApiCostResponseLineItemsInner&gt;**](FreeToolCalculateXApiCostResponseLineItemsInner.md) | One row per billed resource: count × unit price. | [optional] |
| **total_usd** | **Float** | Sum of every line item. | [optional] |
| **link_premium_usd** | **Float** | What the link posts cost on top of the plain post price. | [optional] |
| **notes** | **Array&lt;String&gt;** |  | [optional] |
| **prices_last_verified** | **Date** | When the prices were last checked against the source. | [optional] |
| **source** | **String** |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolCalculateXApiCostResponse.new(
  line_items: null,
  total_usd: null,
  link_premium_usd: null,
  notes: null,
  prices_last_verified: null,
  source: null
)
```

