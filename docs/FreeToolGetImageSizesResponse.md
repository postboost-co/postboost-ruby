# PostBoost::FreeToolGetImageSizesResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **sizes** | [**Array&lt;FreeToolGetImageSizesResponseSizesInner&gt;**](FreeToolGetImageSizesResponseSizesInner.md) |  | [optional] |
| **last_verified** | **Date** | When the data was last checked against its sources. | [optional] |
| **sources** | [**Array&lt;FreeToolGetImageSizesResponseSourcesInner&gt;**](FreeToolGetImageSizesResponseSourcesInner.md) | Sources of the whole dataset (rows may name their own). | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolGetImageSizesResponse.new(
  sizes: null,
  last_verified: null,
  sources: null
)
```

