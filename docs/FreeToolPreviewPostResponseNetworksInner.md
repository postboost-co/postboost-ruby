# PostBoost::FreeToolPreviewPostResponseNetworksInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **key** | **String** |  | [optional] |
| **count** | **Integer** |  | [optional] |
| **limit** | **Integer** |  | [optional] |
| **over** | **Boolean** |  | [optional] |
| **preview** | **String** | What the feed shows before the \&quot;more\&quot; link (approximate; varies by device). | [optional] |
| **folded** | **Boolean** |  | [optional] |
| **min_ratio** | **String** | Tallest image ratio the feed shows uncropped (Instagram: the chosen ratio). Taller images are cropped from the centre. | [optional] |
| **max_ratio** | **String** | Widest image ratio the feed shows uncropped (Instagram: the chosen ratio). Wider images are cropped from the centre. | [optional] |
| **display_ratio** | **Float** | Width / height the card shows the image at, 2 decimals. Only when image_width and image_height are given. | [optional] |
| **cropped** | **Boolean** | Whether the card crops the image. Only when image_width and image_height are given. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolPreviewPostResponseNetworksInner.new(
  key: null,
  count: null,
  limit: null,
  over: null,
  preview: null,
  folded: null,
  min_ratio: null,
  max_ratio: null,
  display_ratio: null,
  cropped: null
)
```

