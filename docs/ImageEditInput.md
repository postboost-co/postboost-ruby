# PostBoost::ImageEditInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **media_uuid** | **String** | UUID of the source media item to edit |  |
| **prompt** | **String** | Describe what to change in the image |  |
| **mask_uuid** | **String** | UUID of a mask image. Transparent areas will be edited. | [optional] |
| **aspect_ratio** | **String** |  | [optional][default to &#39;1:1&#39;] |
| **count** | **Integer** |  | [optional][default to 1] |
| **quality** | **String** |  | [optional][default to &#39;standard&#39;] |

## Example

```ruby
require 'postboost'

instance = PostBoost::ImageEditInput.new(
  media_uuid: null,
  prompt: Make the background a white studio backdrop,
  mask_uuid: null,
  aspect_ratio: null,
  count: null,
  quality: null
)
```

