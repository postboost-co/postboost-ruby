# PostBoost::ImageGenerationResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **images** | [**Array&lt;Media&gt;**](Media.md) |  |  |
| **prompt_used** | **String** |  |  |
| **revised_prompt** | **String** |  | [optional] |
| **aspect_ratio** | **String** |  |  |
| **quality** | **String** |  |  |
| **credits_used** | **Integer** | Text credits only. 0 while the image credit pool is on; &#x60;count × credit_weight&#x60; when it is switched off. |  |
| **credits_remaining** | **Integer** | Text credits left this billing cycle (null &#x3D; no limit). | [optional] |
| **image_credits_used** | **Integer** | Image credits this call spent (1 per image; 0 when the image credit pool is switched off). |  |
| **image_credits_remaining** | **Integer** | Image credits left this month (null &#x3D; no limit, or the image credit pool is switched off). |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::ImageGenerationResponse.new(
  images: null,
  prompt_used: null,
  revised_prompt: null,
  aspect_ratio: 1:1,
  quality: standard,
  credits_used: 0,
  credits_remaining: 45,
  image_credits_used: 1,
  image_credits_remaining: 29
)
```

