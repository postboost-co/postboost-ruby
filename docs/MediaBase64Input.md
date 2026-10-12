# PostBoost::MediaBase64Input

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **content** | **String** | The file as base64. A &#x60;data:&lt;mime&gt;;base64,&#x60; prefix is accepted. At most 20 MB once decoded. |  |
| **filename** | **String** | File name with extension, for example &#x60;cover.png&#x60;. No folders. |  |
| **alt_text** | **String** | Alternative text for accessibility. | [optional] |
| **folder** | **String** | UUID of the media folder to file the upload in. Omit or null for the library root. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::MediaBase64Input.new(
  content: null,
  filename: cover.png,
  alt_text: null,
  folder: null
)
```

