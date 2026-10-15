# PostBoost::FreeToolCleanTextRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **text** | **String** |  |  |
| **dashes** | **String** | What replaces an em or en dash between words: \&quot;, \&quot; (comma), \&quot;-\&quot; (hyphen), \&quot; - \&quot; (spaced) or nothing (keep). Number ranges like 2020–2024 always get a hyphen. | [optional][default to &#39;comma&#39;] |
| **quotes** | **Boolean** | Curly quotes and apostrophes to straight ones. | [optional][default to true] |
| **invisible** | **Boolean** | Remove zero-width characters and soft hyphens; turn non-breaking and thin spaces into normal spaces. | [optional][default to true] |
| **spaces** | **Boolean** | Collapse double spaces between words and remove spaces at line ends. | [optional][default to true] |
| **ellipsis** | **Boolean** | The ellipsis character to three dots. | [optional][default to true] |
| **markdown** | **Boolean** | Strip **bold**, __bold__, *italic* and _italic_ markers, keeping the words. | [optional][default to true] |
| **flag_phrases** | **Boolean** | List common AI phrases (e.g. \&quot;delve\&quot;) with their offsets. They are never changed. | [optional][default to true] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolCleanTextRequest.new(
  text: null,
  dashes: null,
  quotes: null,
  invisible: null,
  spaces: null,
  ellipsis: null,
  markdown: null,
  flag_phrases: null
)
```

