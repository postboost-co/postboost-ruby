# PostBoost::FreeToolPreviewPostRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **text** | **String** |  |  |
| **instagram_ratio** | **String** | Image ratio of the Instagram feed post. | [optional][default to &#39;1:1&#39;] |
| **image_width** | **Integer** | Image width in pixels. Give it with image_height to get display_ratio and cropped per card. | [optional] |
| **image_height** | **Integer** | Image height in pixels. Give it with image_width. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolPreviewPostRequest.new(
  text: null,
  instagram_ratio: null,
  image_width: null,
  image_height: null
)
```

