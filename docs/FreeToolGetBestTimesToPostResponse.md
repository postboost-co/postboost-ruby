# PostBoost::FreeToolGetBestTimesToPostResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **networks** | [**Array&lt;FreeToolGetBestTimesToPostResponseNetworksInner&gt;**](FreeToolGetBestTimesToPostResponseNetworksInner.md) |  | [optional] |
| **last_verified** | **Date** | When the data was last checked against its sources. | [optional] |
| **sources** | [**Array&lt;FreeToolGetImageSizesResponseSourcesInner&gt;**](FreeToolGetImageSizesResponseSourcesInner.md) | Sources of the whole dataset (rows may name their own). | [optional] |
| **per_account** | **String** | Where to get times from your own accounts. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolGetBestTimesToPostResponse.new(
  networks: null,
  last_verified: null,
  sources: null,
  per_account: null
)
```

