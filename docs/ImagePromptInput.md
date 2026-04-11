# PostBoost::ImagePromptInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **caption** | **String** |  |  |
| **platform** | **String** |  |  |
| **template** | **String** |  | [optional] |
| **style** | **String** |  | [optional] |
| **brand_voice** | **String** |  | [optional] |
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
  custom_instructions: null
)
```

