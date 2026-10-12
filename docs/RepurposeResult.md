# PostBoost::RepurposeResult

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **source** | [**RepurposeResultSource**](RepurposeResultSource.md) |  |  |
| **captions** | [**Array&lt;BlogToSocialCaption&gt;**](BlogToSocialCaption.md) |  |  |
| **slides** | [**Array&lt;RepurposeSlide&gt;**](RepurposeSlide.md) | Carousel slides in order (hook first, call to action last). Empty without a carousel. |  |
| **media** | [**RepurposeResultMedia**](RepurposeResultMedia.md) |  | [optional] |
| **post_uuid** | **String** | The draft post; null when &#x60;create_post&#x60; was false. |  |
| **credits_used** | **Integer** |  |  |
| **credits_remaining** | **Integer** | Null for unlimited plans. |  |
| **warnings** | **Array&lt;String&gt;** | Parts that were skipped (for example a network that gets no carousel). |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::RepurposeResult.new(
  source: null,
  captions: null,
  slides: null,
  media: null,
  post_uuid: null,
  credits_used: null,
  credits_remaining: null,
  warnings: null
)
```

