# PostBoost::ImagePromptInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **caption** | **String** |  |  |
| **platform** | **String** |  |  |
| **template** | **String** |  | [optional] |
| **style** | **String** |  | [optional] |
| **brand_voice** | **String** | Free-text tone for the image. When sent, it replaces the stored workspace brand voice for this call. | [optional] |
| **use_brand_voice** | **Boolean** | When &#x60;brand_voice&#x60; is not sent, derive the image tone from the workspace brand voice. Ignored in developer mode (&#x60;prompt&#x60;). | [optional][default to true] |
| **custom_instructions** | **String** |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::ImagePromptInput.new(
  caption: Our summer sale starts today, 30% off everything!,
  platform: instagram,
  template: null,
  style: minimalist,
  brand_voice: friendly,
  use_brand_voice: null,
  custom_instructions: null
)
```

