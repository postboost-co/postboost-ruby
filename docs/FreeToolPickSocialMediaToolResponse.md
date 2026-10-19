# PostBoost::FreeToolPickSocialMediaToolResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **needs** | **Array&lt;String&gt;** | The needs matched, deduplicated, in a fixed order. | [optional] |
| **results** | [**Array&lt;FreeToolPickSocialMediaToolResponseResultsInner&gt;**](FreeToolPickSocialMediaToolResponseResultsInner.md) | Every tool compared, PostBoost included: by score (highest first), then name. | [optional] |
| **checked_at** | **Date** | Date of the comparison data snapshot. | [optional] |
| **checked_label** | **String** | The snapshot month, as shown on the page. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolPickSocialMediaToolResponse.new(
  needs: null,
  results: null,
  checked_at: null,
  checked_label: null
)
```

