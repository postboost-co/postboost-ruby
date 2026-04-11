# PostBoost::ImageGenerateInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **caption** | **String** | Social media caption. Triggers standard mode. Takes priority over prompt. | [optional] |
| **platform** | **String** | Required when caption is provided. | [optional] |
| **template** | **String** |  | [optional] |
| **style** | **String** |  | [optional] |
| **brand_voice** | **String** |  | [optional] |
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
  custom_instructions: null,
  prompt: null,
  aspect_ratio: null,
  count: null,
  quality: null
)
```

