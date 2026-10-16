# PostBoost::FreeToolGenerateQrCodeResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | **String** | The exact string encoded in the code (the link with its UTM tags). | [optional] |
| **svg** | **String** | The QR code as an SVG document. | [optional] |
| **warnings** | **Array&lt;String&gt;** |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolGenerateQrCodeResponse.new(
  data: null,
  svg: null,
  warnings: null
)
```

