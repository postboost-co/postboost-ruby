# PostBoost::BlogToSocialInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **url** | **String** | Blog post URL to scrape. Required if &#x60;title&#x60; and &#x60;excerpt&#x60; are not provided. | [optional] |
| **title** | **String** | Blog post title. Required if &#x60;url&#x60; is not provided. | [optional] |
| **excerpt** | **String** | Blog post summary or excerpt. Required if &#x60;url&#x60; is not provided. | [optional] |
| **image_url** | **String** | Featured image URL for the blog post. When &#x60;create_post&#x60; is &#x60;true&#x60;, the image is imported into the workspace media library and attached to the draft post. If omitted in URL mode, the scraper attempts to extract the &#x60;og:image&#x60; meta tag.  | [optional] |
| **platforms** | **Array&lt;String&gt;** | Target social media platforms. Only connected accounts matching these platforms are used. If omitted, all connected accounts in the workspace are targeted.  | [optional] |
| **account_ids** | **Array&lt;Integer&gt;** | Specific account IDs to generate captions for. Takes precedence over &#x60;platforms&#x60; when both are provided.  | [optional] |
| **tone** | **String** | Writing tone for all generated captions. | [optional][default to &#39;engaging&#39;] |
| **content_length** | **String** | Desired length of the generated captions. | [optional][default to &#39;medium&#39;] |
| **hashtags** | **String** | Hashtag quantity: none (0), few (1-3), some (3-5), many (5+). | [optional][default to &#39;few&#39;] |
| **cta** | **String** | Call-to-action type appended to each caption. | [optional][default to &#39;none&#39;] |
| **language** | **String** | Output language as an ISO 639-1 code (e.g. &#x60;en&#x60;, &#x60;de&#x60;, &#x60;fr&#x60;). Use &#x60;auto&#x60; to match the blog post&#39;s language automatically.  | [optional][default to &#39;auto&#39;] |
| **custom_instructions** | **String** | Additional instructions appended to the AI prompt (e.g. \&quot;always mention our free tier\&quot;). | [optional] |
| **create_post** | **Boolean** | When &#x60;true&#x60;, creates a draft post in the workspace with per-account caption versions. If an image is available, it is imported and attached to the post.  | [optional][default to false] |

## Example

```ruby
require 'postboost'

instance = PostBoost::BlogToSocialInput.new(
  url: https://example.com/blog/my-post,
  title: 10 Tips for Better Social Media,
  excerpt: Social media success starts with consistency and knowing your audience...,
  image_url: https://example.com/images/post-cover.jpg,
  platforms: [x, linkedin],
  account_ids: [5, 12],
  tone: professional,
  content_length: medium,
  hashtags: few,
  cta: link,
  language: auto,
  custom_instructions: Always mention that PostBoost supports 12+ platforms.,
  create_post: null
)
```

