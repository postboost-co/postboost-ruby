# PostBoost::FreeToolGetVideoSpecsResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **specs** | [**Array&lt;FreeToolGetVideoSpecsResponseSpecsInner&gt;**](FreeToolGetVideoSpecsResponseSpecsInner.md) |  | [optional] |
| **last_verified** | **Date** | When the data was last checked against its sources. | [optional] |
| **sources** | [**Array&lt;FreeToolGetImageSizesResponseSourcesInner&gt;**](FreeToolGetImageSizesResponseSourcesInner.md) | Sources of the whole dataset (rows may name their own). | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolGetVideoSpecsResponse.new(
  specs: null,
  last_verified: null,
  sources: null
)
```

