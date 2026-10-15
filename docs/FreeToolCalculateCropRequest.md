# PostBoost::FreeToolCalculateCropRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **width** | **Integer** | Source image width in pixels. |  |
| **height** | **Integer** | Source image height in pixels. |  |
| **network** | **String** | Network key from getImageSizes (&#x60;network_key&#x60;), e.g. &#x60;instagram&#x60;. With &#x60;format&#x60;, picks the target size. | [optional] |
| **format** | **String** | Format key from getImageSizes (&#x60;format_key&#x60;), e.g. &#x60;feed-square&#x60;. | [optional] |
| **target_width** | **Integer** | Target width in pixels, instead of &#x60;network&#x60; + &#x60;format&#x60;. | [optional] |
| **target_height** | **Integer** | Target height in pixels, instead of &#x60;network&#x60; + &#x60;format&#x60;. | [optional] |
| **fit** | **String** | &#x60;cover&#x60; crops to fill the target; &#x60;contain&#x60; keeps the whole image and centres it. | [optional][default to &#39;cover&#39;] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolCalculateCropRequest.new(
  width: null,
  height: null,
  network: null,
  format: null,
  target_width: null,
  target_height: null,
  fit: null
)
```

