# PostBoost::RepurposeInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **source_type** | **String** |  |  |
| **url** | **String** | Article URL (&#x60;url&#x60;) or YouTube video URL (&#x60;youtube&#x60;). For &#x60;text&#x60;, an optional link to mention. | [optional] |
| **pdf_url** | **String** | Public URL of a PDF (&#x60;pdf&#x60;), at most 20 MB. | [optional] |
| **title** | **String** | Required for &#x60;text&#x60;. For &#x60;youtube&#x60;, overrides the video title. | [optional] |
| **text** | **String** | Required for &#x60;text&#x60;. Long sources are cut to about 12,000 characters. | [optional] |
| **transcript** | **String** | Video transcript for &#x60;youtube&#x60;. | [optional] |
| **platforms** | **Array&lt;String&gt;** | Limit to connected accounts of these networks. Ignored when &#x60;account_ids&#x60; is set. | [optional] |
| **account_ids** | **Array&lt;Integer&gt;** | Target accounts. Default is every connected account. | [optional] |
| **tone** | **String** |  | [optional][default to &#39;engaging&#39;] |
| **content_length** | **String** |  | [optional][default to &#39;medium&#39;] |
| **hashtags** | **String** |  | [optional][default to &#39;few&#39;] |
| **cta** | **String** |  | [optional][default to &#39;none&#39;] |
| **language** | **String** |  | [optional][default to &#39;auto&#39;] |
| **custom_instructions** | **String** |  | [optional] |
| **carousel** | **Boolean** | Render carousel slides (one extra AI credit for the outline). | [optional][default to true] |
| **slide_count** | **Integer** | Total slides including the hook and call-to-action slides. | [optional][default to 7] |
| **theme** | [**RepurposeInputTheme**](RepurposeInputTheme.md) |  | [optional] |
| **create_post** | **Boolean** | Create the draft post. &#x60;false&#x60; returns captions and slides only. | [optional][default to true] |
| **use_brand_voice** | **Boolean** |  | [optional][default to true] |
| **async** | **Boolean** | Answer &#x60;202&#x60; with a run id right away instead of waiting up to 20 seconds for the result. | [optional][default to false] |

## Example

```ruby
require 'postboost'

instance = PostBoost::RepurposeInput.new(
  source_type: null,
  url: null,
  pdf_url: null,
  title: null,
  text: null,
  transcript: null,
  platforms: null,
  account_ids: null,
  tone: null,
  content_length: null,
  hashtags: null,
  cta: null,
  language: null,
  custom_instructions: null,
  carousel: null,
  slide_count: null,
  theme: null,
  create_post: null,
  use_brand_voice: null,
  async: null
)
```

