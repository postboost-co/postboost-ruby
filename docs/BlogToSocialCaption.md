# PostBoost::BlogToSocialCaption

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | ID of the social account this caption was generated for. | [optional] |
| **provider** | **String** | Social media platform identifier. | [optional] |
| **content** | **String** | The generated caption text. &#x60;null&#x60; if generation failed for this account. | [optional] |
| **character_count** | **Integer** | Character count of the generated content. &#x60;null&#x60; if generation failed. | [optional] |
| **character_limit** | **Integer** | Maximum allowed character count for this platform. | [optional] |
| **error** | **String** | Error message if caption generation failed for this account. &#x60;null&#x60; on success. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::BlogToSocialCaption.new(
  account_id: 5,
  provider: x,
  content: Unlock better social media results with these 10 proven tips. #SocialMedia #Marketing,
  character_count: 87,
  character_limit: 280,
  error: null
)
```

