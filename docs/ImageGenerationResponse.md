# PostBoost::ImageGenerationResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **images** | [**Array&lt;Media&gt;**](Media.md) |  |  |
| **prompt_used** | **String** |  |  |
| **revised_prompt** | **String** |  | [optional] |
| **aspect_ratio** | **String** |  |  |
| **quality** | **String** |  |  |
| **credits_used** | **Integer** |  |  |
| **credits_remaining** | **Integer** |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::ImageGenerationResponse.new(
  images: null,
  prompt_used: null,
  revised_prompt: null,
  aspect_ratio: 1:1,
  quality: standard,
  credits_used: 5,
  credits_remaining: 45
)
```

