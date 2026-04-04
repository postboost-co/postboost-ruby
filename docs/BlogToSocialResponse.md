# PostBoost::BlogToSocialResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **blog_title** | **String** | The blog post title (scraped or provided directly). | [optional] |
| **blog_excerpt** | **String** | A short excerpt from the blog post content. | [optional] |
| **captions** | [**Array&lt;BlogToSocialCaption&gt;**](BlogToSocialCaption.md) | Generated captions, one per target account. | [optional] |
| **post_uuid** | **String** | UUID of the created draft post. Only present when &#x60;create_post&#x60; was &#x60;true&#x60;. | [optional] |
| **media** | [**BlogToSocialMedia**](BlogToSocialMedia.md) |  | [optional] |
| **credits_used** | **Integer** | Number of AI credits consumed by this request (one per successful caption). | [optional] |
| **credits_remaining** | **Integer** | Remaining AI credits for the current billing period. &#x60;null&#x60; for unlimited plans. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::BlogToSocialResponse.new(
  blog_title: 10 Tips for Better Social Media,
  blog_excerpt: Social media success starts with consistency...,
  captions: null,
  post_uuid: 01942c3d-1234-7abc-8ef0-1234567890ab,
  media: null,
  credits_used: 3,
  credits_remaining: 37
)
```

