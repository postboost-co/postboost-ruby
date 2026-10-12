# PostBoost::BrandVoice

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **business_name** | **String** |  | [optional] |
| **mission** | **String** |  | [optional] |
| **industry** | **String** |  | [optional] |
| **personality** | **String** |  | [optional] |
| **audience** | **Array&lt;String&gt;** |  | [optional] |
| **topics_preferred** | **Array&lt;String&gt;** |  | [optional] |
| **topics_avoided** | **Array&lt;String&gt;** |  | [optional] |
| **tone_formal** | **Integer** |  |  |
| **tone_playful** | **Integer** |  |  |
| **tone_technical** | **Integer** |  |  |
| **emoji_style** | **String** |  |  |
| **hashtag_strategy** | **String** |  |  |
| **avoid_words** | **Array&lt;String&gt;** |  | [optional] |
| **preferred_cta** | **Array&lt;String&gt;** |  | [optional] |
| **example_posts** | **Array&lt;String&gt;** |  | [optional] |
| **updated_at** | **Time** |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::BrandVoice.new(
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
  example_posts: null,
  updated_at: null
)
```

