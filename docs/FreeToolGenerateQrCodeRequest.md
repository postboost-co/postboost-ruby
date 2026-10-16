# PostBoost::FreeToolGenerateQrCodeRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | **String** | The link or text to encode. |  |
| **utm** | [**FreeToolGenerateQrCodeRequestUtm**](FreeToolGenerateQrCodeRequestUtm.md) |  | [optional] |
| **error_correction** | **String** | How much of the code can be damaged and still scan: L 7%, M 15%, Q 25%, H 30%. | [optional][default to &#39;M&#39;] |
| **size** | **Integer** | Width and height of the SVG in pixels. | [optional][default to 512] |
| **foreground** | **String** | Colour of the modules, #RRGGBB. | [optional][default to &#39;#000000&#39;] |
| **background** | **String** | Background colour, #RRGGBB. | [optional][default to &#39;#FFFFFF&#39;] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolGenerateQrCodeRequest.new(
  data: null,
  utm: null,
  error_correction: null,
  size: null,
  foreground: null,
  background: null
)
```

