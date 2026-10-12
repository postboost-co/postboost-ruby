# PostBoost::ImageGenerateInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **caption** | **String** | Social media caption. Triggers standard mode. Takes priority over prompt. | [optional] |
| **platform** | **String** | Required when caption is provided. | [optional] |
| **template** | **String** |  | [optional] |
| **style** | **String** |  | [optional] |
| **brand_voice** | **String** | Free-text tone for the image. When sent, it replaces the stored workspace brand voice for this call. | [optional] |
| **use_brand_voice** | **Boolean** | When &#x60;brand_voice&#x60; is not sent, derive the image tone from the workspace brand voice. Ignored in developer mode (&#x60;prompt&#x60;). | [optional][default to true] |
| **custom_instructions** | **String** |  | [optional] |
| **prompt** | **String** | Developer escape hatch. Bypasses internal prompt builder. Ignored if caption is present. | [optional] |
| **aspect_ratio** | **String** |  | [optional][default to &#39;1:1&#39;] |
| **count** | **Integer** |  | [optional][default to 1] |
| **quality** | **String** |  | [optional][default to &#39;standard&#39;] |

## Example

```ruby
require 'postboost'

instance = PostBoost::ImageGenerateInput.new(
  caption: null,
  platform: instagram,
  template: null,
  style: minimalist,
  brand_voice: friendly,
  use_brand_voice: null,
  custom_instructions: null,
  prompt: null,
  aspect_ratio: null,
  count: null,
  quality: null
)
```

