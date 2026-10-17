# PostBoost::FreeToolCalculateCarouselSlicesRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **width** | **Integer** | Source image width in pixels. |  |
| **height** | **Integer** | Source image height in pixels. |  |
| **slides** | **Integer** | Number of carousel slides, 2 to 10 (the most a carousel published through the Instagram API can hold). |  |
| **ratio** | **String** | Shape of each slide: &#x60;1:1&#x60; (1080 × 1080) or &#x60;4:5&#x60; (1080 × 1350). | [optional][default to &#39;4:5&#39;] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolCalculateCarouselSlicesRequest.new(
  width: null,
  height: null,
  slides: null,
  ratio: null
)
```

