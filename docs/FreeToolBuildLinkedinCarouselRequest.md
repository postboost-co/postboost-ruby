# PostBoost::FreeToolBuildLinkedinCarouselRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **text** | **String** | The post or outline. Blank lines separate slides; a first line starting with # (or a short first line without closing punctuation that is not a list item) is the slide heading; - * • lines become bullets. |  |
| **max_slides** | **Integer** | Most slides to return, 3 to 20. The cover and the CTA slide are always kept. | [optional][default to 10] |
| **size** | **String** | Slide shape: &#x60;4:5&#x60; (1080 × 1350) or &#x60;1:1&#x60; (1080 × 1080). Every page of a LinkedIn document has the same size. | [optional][default to &#39;4:5&#39;] |
| **cover** | **Boolean** | Start with a cover slide: the first heading, or the first line of the text. | [optional][default to true] |
| **cta** | **String** | Text of a closing call-to-action slide. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolBuildLinkedinCarouselRequest.new(
  text: null,
  max_slides: null,
  size: null,
  cover: null,
  cta: null
)
```

