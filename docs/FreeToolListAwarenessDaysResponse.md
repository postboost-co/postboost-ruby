# PostBoost::FreeToolListAwarenessDaysResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **covers** | [**FreeToolListAwarenessDaysResponseCovers**](FreeToolListAwarenessDaysResponseCovers.md) |  | [optional] |
| **total** | **Integer** | Number of entries returned. | [optional] |
| **entries** | [**Array&lt;FreeToolListAwarenessDaysResponseEntriesInner&gt;**](FreeToolListAwarenessDaysResponseEntriesInner.md) |  | [optional] |
| **last_verified** | **Date** | When the data was last checked against its sources. | [optional] |
| **sources** | [**Array&lt;FreeToolGetImageSizesResponseSourcesInner&gt;**](FreeToolGetImageSizesResponseSourcesInner.md) | Sources of the whole dataset (rows may name their own). | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolListAwarenessDaysResponse.new(
  covers: null,
  total: null,
  entries: null,
  last_verified: null,
  sources: null
)
```

