# PostBoost::AIApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**blog_to_social**](AIApi.md#blog_to_social) | **POST** /{workspaceUuid}/ai/blog-to-social | Generate social media captions from a blog post |
| [**image_alt_text**](AIApi.md#image_alt_text) | **POST** /{workspaceUuid}/ai/image-alt-text | Generate alt text for a media image using AI |
| [**image_edit**](AIApi.md#image_edit) | **POST** /{workspaceUuid}/ai/image-edit | Edit an existing media image using AI |
| [**image_generate**](AIApi.md#image_generate) | **POST** /{workspaceUuid}/ai/image-generate | Generate social media images from a caption |
| [**image_prompt**](AIApi.md#image_prompt) | **POST** /{workspaceUuid}/ai/image-prompt | Build an optimized image prompt from a social media caption |
| [**image_variations**](AIApi.md#image_variations) | **POST** /{workspaceUuid}/ai/image-variations | Generate variations of an existing media image |


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

