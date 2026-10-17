# PostBoost::FreeToolCalculateCarouselSlicesResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **slides** | [**Array&lt;FreeToolCalculateCarouselSlicesResponseSlidesInner&gt;**](FreeToolCalculateCarouselSlicesResponseSlidesInner.md) | The part of the source image each slide shows, left to right, in source pixels. | [optional] |
| **output** | [**FreeToolCalculateCarouselSlicesResponseOutput**](FreeToolCalculateCarouselSlicesResponseOutput.md) |  | [optional] |
| **scale** | **Float** | Output pixels per source pixel, 4 decimals. | [optional] |
| **upscaled** | **Boolean** | True when the source is enlarged (scale above 1), which can look soft. | [optional] |
| **warnings** | **Array&lt;String&gt;** | Upscaling and how much of the source is cropped away. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolCalculateCarouselSlicesResponse.new(
  slides: null,
  output: null,
  scale: null,
  upscaled: null,
  warnings: null
)
```

