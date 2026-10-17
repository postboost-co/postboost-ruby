# PostBoost::FreeToolGetSafeZonesRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **platform** | **String** | The app the vertical video is posted to. Approximate: platforms do not publish official overlay sizes for organic posts, and the UI varies by device and app version. The boxes come from each platform&#39;s guidance for vertical video ads. Sources last verified 2026-10-17. |  |
| **width** | **Integer** | Frame width in pixels. The boxes are measured on 1080 × 1920 and scaled to the frame. | [optional][default to 1080] |
| **height** | **Integer** | Frame height in pixels. | [optional][default to 1920] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolGetSafeZonesRequest.new(
  platform: null,
  width: null,
  height: null
)
```

