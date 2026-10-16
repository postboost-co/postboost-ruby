# PostBoost::FreeToolCheckReadabilityResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **supported** | **Boolean** | False for a language other than English: no scores, hints or suggestions. | [optional] |
| **note** | **String** | Why the text was not scored, or null. | [optional] |
| **flesch_reading_ease** | **Float** | Flesch reading ease, one decimal: higher is easier, 60-70 is plain English. Null when not scored. | [optional] |
| **flesch_kincaid_grade** | **Float** | Flesch-Kincaid grade level, one decimal: the US school grade that can read the text. Null when not scored. | [optional] |
| **sentences** | **Integer** | Sentences with at least one word. | [optional] |
| **words** | **Integer** | Words, not counting hashtags, @mentions, links and emoji. | [optional] |
| **syllables** | **Integer** | Syllables, by the heuristic described in the docs. | [optional] |
| **avg_words_per_sentence** | **Float** | Words per sentence, one decimal. | [optional] |
| **long_sentences** | [**Array&lt;FreeToolCheckReadabilityResponseLongSentencesInner&gt;**](FreeToolCheckReadabilityResponseLongSentencesInner.md) | Sentences of more than 25 words. | [optional] |
| **passive_hints** | **Integer** | Possible passive phrases (\&quot;was written\&quot;, \&quot;is being reviewed\&quot;). A hint, not a grammar check. | [optional] |
| **emoji_count** | **Integer** | Emoji (Extended_Pictographic characters). | [optional] |
| **hashtag_count** | **Integer** | Hashtags. | [optional] |
| **suggestions** | **Array&lt;String&gt;** | Plain fixes, e.g. which sentence to split. Empty when the text reads easily. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolCheckReadabilityResponse.new(
  supported: null,
  note: null,
  flesch_reading_ease: null,
  flesch_kincaid_grade: null,
  sentences: null,
  words: null,
  syllables: null,
  avg_words_per_sentence: null,
  long_sentences: null,
  passive_hints: null,
  emoji_count: null,
  hashtag_count: null,
  suggestions: null
)
```

