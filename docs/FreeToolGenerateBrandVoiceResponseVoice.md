# PostBoost::FreeToolGenerateBrandVoiceResponseVoice

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **business_name** | **String** | Your input, or null. | [optional] |
| **mission** | **String** | Only when the posts state it, else null. | [optional] |
| **industry** | **String** | Your input, or null. | [optional] |
| **personality** | **String** | How the brand sounds. | [optional] |
| **audience** | **Array&lt;String&gt;** | Who the posts speak to. At most 8 items. | [optional] |
| **topics_preferred** | **Array&lt;String&gt;** | Topics the posts come back to. At most 8 items. | [optional] |
| **topics_avoided** | **Array&lt;String&gt;** | Topics the posts clearly steer away from; often empty. At most 8 items. | [optional] |
| **tone_formal** | **Integer** | 1 very casual to 5 very formal, 3 neutral. | [optional] |
| **tone_playful** | **Integer** | 1 very serious to 5 very playful, 3 neutral. | [optional] |
| **tone_technical** | **Integer** | 1 very simple to 5 very technical, 3 neutral. | [optional] |
| **emoji_style** | **String** |  | [optional] |
| **hashtag_strategy** | **String** |  | [optional] |
| **avoid_words** | **Array&lt;String&gt;** | Words the posts clearly avoid; often empty. At most 8 items. | [optional] |
| **preferred_cta** | **Array&lt;String&gt;** | Calls to action the posts use. At most 8 items. | [optional] |
| **example_posts** | **Array&lt;String&gt;** | Up to 5 of your posts that sound most typical, exactly as given. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolGenerateBrandVoiceResponseVoice.new(
  business_name: null,
  mission: null,
  industry: null,
  personality: null,
  audience: null,
  topics_preferred: null,
  topics_avoided: null,
  tone_formal: null,
  tone_playful: null,
  tone_technical: null,
  emoji_style: null,
  hashtag_strategy: null,
  avoid_words: null,
  preferred_cta: null,
  example_posts: null
)
```

