# PostBoost::BrandVoiceInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **business_name** | **String** |  | [optional] |
| **mission** | **String** |  | [optional] |
| **industry** | **String** |  | [optional] |
| **personality** | **String** | How the brand sounds. The first sentence also feeds image prompts. | [optional] |
| **audience** | **Array&lt;String&gt;** |  | [optional] |
| **topics_preferred** | **Array&lt;String&gt;** |  | [optional] |
| **topics_avoided** | **Array&lt;String&gt;** |  | [optional] |
| **tone_formal** | **Integer** | 1 very casual, 3 neutral, 5 very formal. | [optional] |
| **tone_playful** | **Integer** | 1 strictly serious, 3 neutral, 5 very playful. | [optional] |
| **tone_technical** | **Integer** | 1 very simple, 3 neutral, 5 highly technical. | [optional] |
| **emoji_style** | **String** |  | [optional] |
| **hashtag_strategy** | **String** |  | [optional] |
| **avoid_words** | **Array&lt;String&gt;** |  | [optional] |
| **preferred_cta** | **Array&lt;String&gt;** |  | [optional] |
| **example_posts** | **Array&lt;String&gt;** |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::BrandVoiceInput.new(
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

