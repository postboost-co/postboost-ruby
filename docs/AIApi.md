# PostBoost::AIApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**blog_to_social**](AIApi.md#blog_to_social) | **POST** /{workspaceUuid}/ai/blog-to-social | Generate social media captions from a blog post |
| [**delete_brand_voice**](AIApi.md#delete_brand_voice) | **DELETE** /{workspaceUuid}/brand-voice | Delete the brand voice |
| [**get_ai_usage**](AIApi.md#get_ai_usage) | **GET** /{workspaceUuid}/usage/ai | AI credit usage |
| [**get_brand_voice**](AIApi.md#get_brand_voice) | **GET** /{workspaceUuid}/brand-voice | Get the brand voice |
| [**image_alt_text**](AIApi.md#image_alt_text) | **POST** /{workspaceUuid}/ai/image-alt-text | Generate alt text for a media image using AI |
| [**image_edit**](AIApi.md#image_edit) | **POST** /{workspaceUuid}/ai/image-edit | Edit an existing media image using AI |
| [**image_generate**](AIApi.md#image_generate) | **POST** /{workspaceUuid}/ai/image-generate | Generate social media images from a caption |
| [**image_prompt**](AIApi.md#image_prompt) | **POST** /{workspaceUuid}/ai/image-prompt | Build an optimized image prompt from a social media caption |
| [**image_variations**](AIApi.md#image_variations) | **POST** /{workspaceUuid}/ai/image-variations | Generate variations of an existing media image |
| [**learn_brand_voice**](AIApi.md#learn_brand_voice) | **POST** /{workspaceUuid}/brand-voice/learn | Learn a brand voice from past posts |
| [**repurpose_content**](AIApi.md#repurpose_content) | **POST** /{workspaceUuid}/ai/repurpose | Repurpose long-form content into a draft post set with a carousel |
| [**update_brand_voice**](AIApi.md#update_brand_voice) | **PUT** /{workspaceUuid}/brand-voice | Create or update the brand voice |


## blog_to_social

> <BlogToSocial200Response> blog_to_social(workspace_uuid, blog_to_social_input)

Generate social media captions from a blog post

Generates platform-specific social media captions from a blog post URL or directly provided title and excerpt. Each platform generates one caption, which consumes one AI credit from the workspace's monthly allowance.  **Input modes** (at least one required): - **URL mode**: provide `url` and the API scrapes the blog content automatically, including detecting the featured image via `og:image`. - **Direct mode**: provide `title` and `excerpt` directly (no scraping).  If both are provided, direct values take priority.  When `create_post` is `true`, a draft post is created in the workspace with per-account caption versions. If an image is available (from `image_url` or the scraped `og:image`), it is imported into the workspace media library and attached to the draft post. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::AIApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
blog_to_social_input = PostBoost::BlogToSocialInput.new # BlogToSocialInput | 

begin
  # Generate social media captions from a blog post
  result = api_instance.blog_to_social(workspace_uuid, blog_to_social_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AIApi->blog_to_social: #{e}"
end
```

#### Using the blog_to_social_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BlogToSocial200Response>, Integer, Hash)> blog_to_social_with_http_info(workspace_uuid, blog_to_social_input)

```ruby
begin
  # Generate social media captions from a blog post
  data, status_code, headers = api_instance.blog_to_social_with_http_info(workspace_uuid, blog_to_social_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BlogToSocial200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling AIApi->blog_to_social_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **blog_to_social_input** | [**BlogToSocialInput**](BlogToSocialInput.md) |  |  |

### Return type

[**BlogToSocial200Response**](BlogToSocial200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_brand_voice

> Object delete_brand_voice(workspace_uuid)

Delete the brand voice

Removes the workspace's brand voice. AI endpoints then run without one. Admins and members only.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::AIApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.

begin
  # Delete the brand voice
  result = api_instance.delete_brand_voice(workspace_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AIApi->delete_brand_voice: #{e}"
end
```

#### Using the delete_brand_voice_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> delete_brand_voice_with_http_info(workspace_uuid)

```ruby
begin
  # Delete the brand voice
  data, status_code, headers = api_instance.delete_brand_voice_with_http_info(workspace_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue PostBoost::ApiError => e
  puts "Error when calling AIApi->delete_brand_voice_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |

### Return type

**Object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_ai_usage

> <AIUsage> get_ai_usage(workspace_uuid)

AI credit usage

The workspace's AI credits: text credits (captions, rewrites, outlines, alt text; counted per billing cycle) and image credits (one per generated, edited or varied image, and one per repurpose carousel; counted per calendar month, UTC). `limit` and `remaining` are `null` when the workspace has no limit. Readable when credits are used up; costs nothing.  When image credits run out, the image endpoints and carousels answer `429` with `code: image_credits_exhausted`; when text credits run out, the AI endpoints answer `429` with `code: ai_credits_exhausted`. Image endpoint responses also carry `image_credits_used` and `image_credits_remaining`; their `credits_used` counts text credits only. If the image pool is switched off (`image.enabled: false`), images cost text credits as before. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::AIApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.

begin
  # AI credit usage
  result = api_instance.get_ai_usage(workspace_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AIApi->get_ai_usage: #{e}"
end
```

#### Using the get_ai_usage_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AIUsage>, Integer, Hash)> get_ai_usage_with_http_info(workspace_uuid)

```ruby
begin
  # AI credit usage
  data, status_code, headers = api_instance.get_ai_usage_with_http_info(workspace_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AIUsage>
rescue PostBoost::ApiError => e
  puts "Error when calling AIApi->get_ai_usage_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |

### Return type

[**AIUsage**](AIUsage.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_brand_voice

> <GetBrandVoice200Response> get_brand_voice(workspace_uuid)

Get the brand voice

The workspace's brand voice: identity, audience, tone sliders, style rules and example posts. It is the same profile as the Brand Voice page in the app (one per workspace). `data` is `null` when no voice is set. Any workspace member may read it; reading costs no AI credits.  The AI endpoints apply it automatically: `blog-to-social` adds it to the caption instructions, `image-prompt` and `image-generate` turn it into a short visual tone line, and `image-edit` applies it when you send `use_brand_voice: true`. `image-variations` and `image-alt-text` never use it (alt text must describe the image literally). Send `use_brand_voice: false` to skip it on a call; responses report `meta.brand_voice_applied`. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::AIApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.

begin
  # Get the brand voice
  result = api_instance.get_brand_voice(workspace_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AIApi->get_brand_voice: #{e}"
end
```

#### Using the get_brand_voice_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetBrandVoice200Response>, Integer, Hash)> get_brand_voice_with_http_info(workspace_uuid)

```ruby
begin
  # Get the brand voice
  data, status_code, headers = api_instance.get_brand_voice_with_http_info(workspace_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetBrandVoice200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling AIApi->get_brand_voice_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |

### Return type

[**GetBrandVoice200Response**](GetBrandVoice200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## image_alt_text

> <ImageAltText200Response> image_alt_text(workspace_uuid, image_alt_text_input)

Generate alt text for a media image using AI

Analyzes an existing workspace media item and generates accessible alt text. The alt text is saved back to the media record. Costs 1 AI credit per call. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::AIApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
image_alt_text_input = PostBoost::ImageAltTextInput.new({media_uuid: 'media_uuid_example'}) # ImageAltTextInput | 

begin
  # Generate alt text for a media image using AI
  result = api_instance.image_alt_text(workspace_uuid, image_alt_text_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AIApi->image_alt_text: #{e}"
end
```

#### Using the image_alt_text_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ImageAltText200Response>, Integer, Hash)> image_alt_text_with_http_info(workspace_uuid, image_alt_text_input)

```ruby
begin
  # Generate alt text for a media image using AI
  data, status_code, headers = api_instance.image_alt_text_with_http_info(workspace_uuid, image_alt_text_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ImageAltText200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling AIApi->image_alt_text_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **image_alt_text_input** | [**ImageAltTextInput**](ImageAltTextInput.md) |  |  |

### Return type

[**ImageAltText200Response**](ImageAltText200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## image_edit

> <ImageGenerate200Response> image_edit(workspace_uuid, image_edit_input)

Edit an existing media image using AI

Edits an existing workspace media item using the source image and a text prompt. Optionally accepts a mask (transparent areas are replaced). Saves results to the media library. Credits: `count × credit_weight`. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::AIApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
image_edit_input = PostBoost::ImageEditInput.new({media_uuid: 'media_uuid_example', prompt: 'Make the background a white studio backdrop'}) # ImageEditInput | 

begin
  # Edit an existing media image using AI
  result = api_instance.image_edit(workspace_uuid, image_edit_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AIApi->image_edit: #{e}"
end
```

#### Using the image_edit_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ImageGenerate200Response>, Integer, Hash)> image_edit_with_http_info(workspace_uuid, image_edit_input)

```ruby
begin
  # Edit an existing media image using AI
  data, status_code, headers = api_instance.image_edit_with_http_info(workspace_uuid, image_edit_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ImageGenerate200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling AIApi->image_edit_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **image_edit_input** | [**ImageEditInput**](ImageEditInput.md) |  |  |

### Return type

[**ImageGenerate200Response**](ImageGenerate200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## image_generate

> <ImageGenerate200Response> image_generate(workspace_uuid, image_generate_input)

Generate social media images from a caption

Generates one or more images and saves them immediately to the workspace media library.  **Standard mode** (recommended): provide `caption` + `platform`. PostBoost builds a professional image prompt internally using platform-specific templates. No prompt engineering required.  **Developer mode**: provide `prompt` directly to bypass prompt building. If both `caption` and `prompt` are sent, standard mode runs.  Credits: `count x credit_weight` (default: 5 per image). 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::AIApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
image_generate_input = PostBoost::ImageGenerateInput.new # ImageGenerateInput | 

begin
  # Generate social media images from a caption
  result = api_instance.image_generate(workspace_uuid, image_generate_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AIApi->image_generate: #{e}"
end
```

#### Using the image_generate_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ImageGenerate200Response>, Integer, Hash)> image_generate_with_http_info(workspace_uuid, image_generate_input)

```ruby
begin
  # Generate social media images from a caption
  data, status_code, headers = api_instance.image_generate_with_http_info(workspace_uuid, image_generate_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ImageGenerate200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling AIApi->image_generate_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **image_generate_input** | [**ImageGenerateInput**](ImageGenerateInput.md) |  |  |

### Return type

[**ImageGenerate200Response**](ImageGenerate200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## image_prompt

> <ImagePrompt200Response> image_prompt(workspace_uuid, image_prompt_input)

Build an optimized image prompt from a social media caption

Builds a professional image generation prompt from a caption and platform. No image is generated. Use this to preview the prompt before calling `image-generate`. Costs 1 AI credit per call.  When `image-generate` builds the prompt internally (standard mode), no credit is charged for the prompt step. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::AIApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
image_prompt_input = PostBoost::ImagePromptInput.new({caption: 'Our summer sale starts today, 30% off everything!', platform: 'instagram'}) # ImagePromptInput | 

begin
  # Build an optimized image prompt from a social media caption
  result = api_instance.image_prompt(workspace_uuid, image_prompt_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AIApi->image_prompt: #{e}"
end
```

#### Using the image_prompt_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ImagePrompt200Response>, Integer, Hash)> image_prompt_with_http_info(workspace_uuid, image_prompt_input)

```ruby
begin
  # Build an optimized image prompt from a social media caption
  data, status_code, headers = api_instance.image_prompt_with_http_info(workspace_uuid, image_prompt_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ImagePrompt200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling AIApi->image_prompt_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **image_prompt_input** | [**ImagePromptInput**](ImagePromptInput.md) |  |  |

### Return type

[**ImagePrompt200Response**](ImagePrompt200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## image_variations

> <ImageVariations200Response> image_variations(workspace_uuid, image_variations_input)

Generate variations of an existing media image

Creates one or more variations of an existing workspace media item. Saves results to the media library. Credits: `count × credit_weight`. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::AIApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
image_variations_input = PostBoost::ImageVariationsInput.new({media_uuid: 'media_uuid_example'}) # ImageVariationsInput | 

begin
  # Generate variations of an existing media image
  result = api_instance.image_variations(workspace_uuid, image_variations_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AIApi->image_variations: #{e}"
end
```

#### Using the image_variations_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ImageVariations200Response>, Integer, Hash)> image_variations_with_http_info(workspace_uuid, image_variations_input)

```ruby
begin
  # Generate variations of an existing media image
  data, status_code, headers = api_instance.image_variations_with_http_info(workspace_uuid, image_variations_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ImageVariations200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling AIApi->image_variations_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **image_variations_input** | [**ImageVariationsInput**](ImageVariationsInput.md) |  |  |

### Return type

[**ImageVariations200Response**](ImageVariations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## learn_brand_voice

> <LearnBrandVoiceResponse> learn_brand_voice(workspace_uuid, opts)

Learn a brand voice from past posts

Reads the workspace's latest published posts (original text) and proposes a brand voice in the same shape as `GET /brand-voice`. Returns a draft and saves nothing unless `apply: true`.  Without `overwrite`, learned values only fill fields that are empty (tone sliders and styles still at their defaults count as empty); with `overwrite: true` they replace them. The first five sampled posts become `example_posts`. Needs at least 3 published posts (`422`, `code: not_enough_posts`). Costs one AI text credit per AI call (one retry when the reply is not usable). Admins and members only. A key limited to some accounts must send `account_ids`; only posts whose accounts are all among them are read. `apply` also needs the `write` ability. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::AIApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
opts = {
  learn_brand_voice_input: PostBoost::LearnBrandVoiceInput.new # LearnBrandVoiceInput | 
}

begin
  # Learn a brand voice from past posts
  result = api_instance.learn_brand_voice(workspace_uuid, opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AIApi->learn_brand_voice: #{e}"
end
```

#### Using the learn_brand_voice_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<LearnBrandVoiceResponse>, Integer, Hash)> learn_brand_voice_with_http_info(workspace_uuid, opts)

```ruby
begin
  # Learn a brand voice from past posts
  data, status_code, headers = api_instance.learn_brand_voice_with_http_info(workspace_uuid, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <LearnBrandVoiceResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling AIApi->learn_brand_voice_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **learn_brand_voice_input** | [**LearnBrandVoiceInput**](LearnBrandVoiceInput.md) |  | [optional] |

### Return type

[**LearnBrandVoiceResponse**](LearnBrandVoiceResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## repurpose_content

> <RepurposeContent200Response> repurpose_content(workspace_uuid, repurpose_input, opts)

Repurpose long-form content into a draft post set with a carousel

Turns an article URL, a YouTube video, a PDF or pasted text into one **draft** post with a caption for every target account, plus a carousel of rendered slide images (hook, 1 to 6 idea slides, call to action; 1080×1350 PNG). Nothing is published or scheduled.  **Sources** (`source_type`): - `url`: the article is fetched and its main text extracted. - `youtube`: title, description and chapters come from YouTube; send the transcript in   `transcript` for better results (required when the description is short). - `pdf`: `pdf_url` must be a public PDF of at most 20 MB; the first 30 pages are read. - `text`: send `title` and `text`.  **Carousel per network**: Instagram, Facebook, Threads up to 10 slides; LinkedIn up to 9; X and Bluesky up to 4; other networks get the cover slide; YouTube and TikTok get none (listed in `warnings`). Without a carousel, the source image (article image or video thumbnail) is attached when available.  **AI credits**: one per target account plus one for the carousel outline. Slides are drawn without AI and cost nothing. The workspace brand voice applies unless `use_brand_voice` is `false`. Send an `Idempotency-Key` so a retried call does not create a second draft. Limited to 10 calls per minute. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::AIApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
repurpose_input = PostBoost::RepurposeInput.new({source_type: 'url'}) # RepurposeInput | 
opts = {
  idempotency_key: 'idempotency_key_example' # String | Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with `Idempotent-Replayed: true` and has no further effect. Keys are scoped to your user, the workspace, the method and the path. 
}

begin
  # Repurpose long-form content into a draft post set with a carousel
  result = api_instance.repurpose_content(workspace_uuid, repurpose_input, opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AIApi->repurpose_content: #{e}"
end
```

#### Using the repurpose_content_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<RepurposeContent200Response>, Integer, Hash)> repurpose_content_with_http_info(workspace_uuid, repurpose_input, opts)

```ruby
begin
  # Repurpose long-form content into a draft post set with a carousel
  data, status_code, headers = api_instance.repurpose_content_with_http_info(workspace_uuid, repurpose_input, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <RepurposeContent200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling AIApi->repurpose_content_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **repurpose_input** | [**RepurposeInput**](RepurposeInput.md) |  |  |
| **idempotency_key** | **String** | Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with &#x60;Idempotent-Replayed: true&#x60; and has no further effect. Keys are scoped to your user, the workspace, the method and the path.  | [optional] |

### Return type

[**RepurposeContent200Response**](RepurposeContent200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_brand_voice

> <GetBrandVoice200Response> update_brand_voice(workspace_uuid, brand_voice_input)

Create or update the brand voice

Creates the workspace's brand voice or updates it. Fields you leave out keep their current value. Admins and members only (not viewers); the workspace must have AI enabled. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::AIApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
brand_voice_input = PostBoost::BrandVoiceInput.new # BrandVoiceInput | 

begin
  # Create or update the brand voice
  result = api_instance.update_brand_voice(workspace_uuid, brand_voice_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AIApi->update_brand_voice: #{e}"
end
```

#### Using the update_brand_voice_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetBrandVoice200Response>, Integer, Hash)> update_brand_voice_with_http_info(workspace_uuid, brand_voice_input)

```ruby
begin
  # Create or update the brand voice
  data, status_code, headers = api_instance.update_brand_voice_with_http_info(workspace_uuid, brand_voice_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetBrandVoice200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling AIApi->update_brand_voice_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **brand_voice_input** | [**BrandVoiceInput**](BrandVoiceInput.md) |  |  |

### Return type

[**GetBrandVoice200Response**](GetBrandVoice200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

