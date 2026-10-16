# PostBoost::FreeToolFormatInstagramCaptionRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **text** | **String** |  |  |
| **spacer** | **String** | What fills a blank line: braille (U+2800 Braille blank, shows as an empty line) or dot (a line with \&quot;.\&quot;). | [optional][default to &#39;braille&#39;] |
| **hashtags_to_end** | **Boolean** | Move the hashtags that end a line to the bottom, after three spacer lines. A hashtag inside a sentence stays where it is. | [optional][default to false] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolFormatInstagramCaptionRequest.new(
  text: null,
  spacer: null,
  hashtags_to_end: null
)
```

