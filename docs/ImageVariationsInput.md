# PostBoost::ImageVariationsInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **media_uuid** | **String** |  |  |
| **aspect_ratio** | **String** |  | [optional][default to &#39;1:1&#39;] |
| **count** | **Integer** |  | [optional][default to 1] |
| **quality** | **String** |  | [optional][default to &#39;standard&#39;] |

## Example

```ruby
require 'postboost'

instance = PostBoost::ImageVariationsInput.new(
  media_uuid: null,
  aspect_ratio: null,
  count: null,
  quality: null
)
```

