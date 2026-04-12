# PostBoost::ImageVariationsResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **images** | [**Array&lt;Media&gt;**](Media.md) |  |  |
| **aspect_ratio** | **String** |  |  |
| **quality** | **String** |  |  |
| **credits_used** | **Integer** |  |  |
| **credits_remaining** | **Integer** |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::ImageVariationsResponse.new(
  images: null,
  aspect_ratio: 1:1,
  quality: standard,
  credits_used: 5,
  credits_remaining: 45
)
```

