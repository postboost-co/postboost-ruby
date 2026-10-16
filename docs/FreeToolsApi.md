# PostBoost::FreeToolsApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**build_utm_url**](FreeToolsApi.md#build_utm_url) | **POST** /tools/utm-builder | Build a UTM-tagged campaign URL |
| [**calculate_aspect_ratio**](FreeToolsApi.md#calculate_aspect_ratio) | **POST** /tools/aspect-ratio-calculator | Calculate an aspect ratio, or the missing side of an image at a given ratio |
| [**calculate_crop**](FreeToolsApi.md#calculate_crop) | **POST** /tools/social-media-image-sizes/crop | Calculate the crop box that fits an image to a social media size |
| [**calculate_engagement_rate**](FreeToolsApi.md#calculate_engagement_rate) | **POST** /tools/engagement-rate-calculator | Calculate an engagement rate |
| [**check_post**](FreeToolsApi.md#check_post) | **POST** /tools/social-media-post-checker | Check a post against each network&#39;s publishing rules |
| [**clean_text**](FreeToolsApi.md#clean_text) | **POST** /tools/ai-text-cleaner | Clean AI-written text: dashes, quotes, invisible characters, markdown |
| [**count_characters**](FreeToolsApi.md#count_characters) | **POST** /tools/social-media-character-counter | Count characters as each network counts them |
| [**format_linked_in_post**](FreeToolsApi.md#format_linked_in_post) | **POST** /tools/linkedin-post-formatter | Format a LinkedIn post with bold, italic and lists |
| [**generate_caption**](FreeToolsApi.md#generate_caption) | **POST** /tools/instagram-caption-generator | Write three post captions for a topic with AI (needs a token, spends AI credits) |
| [**generate_fancy_text**](FreeToolsApi.md#generate_fancy_text) | **POST** /tools/fancy-text-generator | Convert text to fancy Unicode styles |
| [**generate_hashtags**](FreeToolsApi.md#generate_hashtags) | **POST** /tools/instagram-hashtag-generator | Generate hashtags for a post topic with AI (needs a token, spends AI credits) |
| [**get_best_times_to_post**](FreeToolsApi.md#get_best_times_to_post) | **GET** /tools/best-time-to-post | Get the best times to post per network from published studies, with sources |
| [**get_image_sizes**](FreeToolsApi.md#get_image_sizes) | **GET** /tools/social-media-image-sizes | Get social media image sizes per network, each with its source |
| [**list_free_tools**](FreeToolsApi.md#list_free_tools) | **GET** /tools | List the free tools |
| [**preview_post**](FreeToolsApi.md#preview_post) | **POST** /tools/social-media-post-preview | Preview where a post folds and when its image is cropped on Instagram, X, LinkedIn and Facebook |
| [**split_thread**](FreeToolsApi.md#split_thread) | **POST** /tools/x-thread-maker | Split long text into a thread |


## build_utm_url

> <FreeToolBuildUtmUrlResponse> build_utm_url(free_tool_build_utm_url_request)

Build a UTM-tagged campaign URL

Build a UTM-tagged campaign URL. The same logic as the free web tool at https://postboost.co/tools/utm-builder. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
free_tool_build_utm_url_request = PostBoost::FreeToolBuildUtmUrlRequest.new({url: 'url_example'}) # FreeToolBuildUtmUrlRequest | 

begin
  # Build a UTM-tagged campaign URL
  result = api_instance.build_utm_url(free_tool_build_utm_url_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->build_utm_url: #{e}"
end
```

#### Using the build_utm_url_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolBuildUtmUrlResponse>, Integer, Hash)> build_utm_url_with_http_info(free_tool_build_utm_url_request)

```ruby
begin
  # Build a UTM-tagged campaign URL
  data, status_code, headers = api_instance.build_utm_url_with_http_info(free_tool_build_utm_url_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolBuildUtmUrlResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->build_utm_url_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_build_utm_url_request** | [**FreeToolBuildUtmUrlRequest**](FreeToolBuildUtmUrlRequest.md) |  |  |

### Return type

[**FreeToolBuildUtmUrlResponse**](FreeToolBuildUtmUrlResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## calculate_aspect_ratio

> <FreeToolCalculateAspectRatioResponse> calculate_aspect_ratio(free_tool_calculate_aspect_ratio_request)

Calculate an aspect ratio, or the missing side of an image at a given ratio

Calculate an aspect ratio, or the missing side of an image at a given ratio. The same logic as the free web tool at https://postboost.co/tools/aspect-ratio-calculator. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
free_tool_calculate_aspect_ratio_request = PostBoost::FreeToolCalculateAspectRatioRequest.new # FreeToolCalculateAspectRatioRequest | 

begin
  # Calculate an aspect ratio, or the missing side of an image at a given ratio
  result = api_instance.calculate_aspect_ratio(free_tool_calculate_aspect_ratio_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->calculate_aspect_ratio: #{e}"
end
```

#### Using the calculate_aspect_ratio_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolCalculateAspectRatioResponse>, Integer, Hash)> calculate_aspect_ratio_with_http_info(free_tool_calculate_aspect_ratio_request)

```ruby
begin
  # Calculate an aspect ratio, or the missing side of an image at a given ratio
  data, status_code, headers = api_instance.calculate_aspect_ratio_with_http_info(free_tool_calculate_aspect_ratio_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolCalculateAspectRatioResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->calculate_aspect_ratio_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_calculate_aspect_ratio_request** | [**FreeToolCalculateAspectRatioRequest**](FreeToolCalculateAspectRatioRequest.md) |  |  |

### Return type

[**FreeToolCalculateAspectRatioResponse**](FreeToolCalculateAspectRatioResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## calculate_crop

> <FreeToolCalculateCropResponse> calculate_crop(free_tool_calculate_crop_request)

Calculate the crop box that fits an image to a social media size

Calculate the crop box that fits an image to a social media size. The same logic as the free web tool at https://postboost.co/tools/social-media-image-sizes. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
free_tool_calculate_crop_request = PostBoost::FreeToolCalculateCropRequest.new({width: 37, height: 37}) # FreeToolCalculateCropRequest | 

begin
  # Calculate the crop box that fits an image to a social media size
  result = api_instance.calculate_crop(free_tool_calculate_crop_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->calculate_crop: #{e}"
end
```

#### Using the calculate_crop_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolCalculateCropResponse>, Integer, Hash)> calculate_crop_with_http_info(free_tool_calculate_crop_request)

```ruby
begin
  # Calculate the crop box that fits an image to a social media size
  data, status_code, headers = api_instance.calculate_crop_with_http_info(free_tool_calculate_crop_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolCalculateCropResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->calculate_crop_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_calculate_crop_request** | [**FreeToolCalculateCropRequest**](FreeToolCalculateCropRequest.md) |  |  |

### Return type

[**FreeToolCalculateCropResponse**](FreeToolCalculateCropResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## calculate_engagement_rate

> <FreeToolCalculateEngagementRateResponse> calculate_engagement_rate(free_tool_calculate_engagement_rate_request)

Calculate an engagement rate

Calculate an engagement rate. The same logic as the free web tool at https://postboost.co/tools/engagement-rate-calculator. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
free_tool_calculate_engagement_rate_request = PostBoost::FreeToolCalculateEngagementRateRequest.new({base: 37}) # FreeToolCalculateEngagementRateRequest | 

begin
  # Calculate an engagement rate
  result = api_instance.calculate_engagement_rate(free_tool_calculate_engagement_rate_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->calculate_engagement_rate: #{e}"
end
```

#### Using the calculate_engagement_rate_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolCalculateEngagementRateResponse>, Integer, Hash)> calculate_engagement_rate_with_http_info(free_tool_calculate_engagement_rate_request)

```ruby
begin
  # Calculate an engagement rate
  data, status_code, headers = api_instance.calculate_engagement_rate_with_http_info(free_tool_calculate_engagement_rate_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolCalculateEngagementRateResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->calculate_engagement_rate_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_calculate_engagement_rate_request** | [**FreeToolCalculateEngagementRateRequest**](FreeToolCalculateEngagementRateRequest.md) |  |  |

### Return type

[**FreeToolCalculateEngagementRateResponse**](FreeToolCalculateEngagementRateResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## check_post

> <FreeToolCheckPostResponse> check_post(free_tool_check_post_request)

Check a post against each network's publishing rules

Check a post against each network's publishing rules. The same logic as the free web tool at https://postboost.co/tools/social-media-post-checker. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
free_tool_check_post_request = PostBoost::FreeToolCheckPostRequest.new({networks: ['x']}) # FreeToolCheckPostRequest | 

begin
  # Check a post against each network's publishing rules
  result = api_instance.check_post(free_tool_check_post_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->check_post: #{e}"
end
```

#### Using the check_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolCheckPostResponse>, Integer, Hash)> check_post_with_http_info(free_tool_check_post_request)

```ruby
begin
  # Check a post against each network's publishing rules
  data, status_code, headers = api_instance.check_post_with_http_info(free_tool_check_post_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolCheckPostResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->check_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_check_post_request** | [**FreeToolCheckPostRequest**](FreeToolCheckPostRequest.md) |  |  |

### Return type

[**FreeToolCheckPostResponse**](FreeToolCheckPostResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## clean_text

> <FreeToolCleanTextResponse> clean_text(free_tool_clean_text_request)

Clean AI-written text: dashes, quotes, invisible characters, markdown

Clean AI-written text: dashes, quotes, invisible characters, markdown. The same logic as the free web tool at https://postboost.co/tools/ai-text-cleaner. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
free_tool_clean_text_request = PostBoost::FreeToolCleanTextRequest.new({text: 'text_example'}) # FreeToolCleanTextRequest | 

begin
  # Clean AI-written text: dashes, quotes, invisible characters, markdown
  result = api_instance.clean_text(free_tool_clean_text_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->clean_text: #{e}"
end
```

#### Using the clean_text_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolCleanTextResponse>, Integer, Hash)> clean_text_with_http_info(free_tool_clean_text_request)

```ruby
begin
  # Clean AI-written text: dashes, quotes, invisible characters, markdown
  data, status_code, headers = api_instance.clean_text_with_http_info(free_tool_clean_text_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolCleanTextResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->clean_text_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_clean_text_request** | [**FreeToolCleanTextRequest**](FreeToolCleanTextRequest.md) |  |  |

### Return type

[**FreeToolCleanTextResponse**](FreeToolCleanTextResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## count_characters

> <FreeToolCountCharactersResponse> count_characters(free_tool_count_characters_request)

Count characters as each network counts them

Count characters as each network counts them. The same logic as the free web tool at https://postboost.co/tools/social-media-character-counter. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
free_tool_count_characters_request = PostBoost::FreeToolCountCharactersRequest.new # FreeToolCountCharactersRequest | 

begin
  # Count characters as each network counts them
  result = api_instance.count_characters(free_tool_count_characters_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->count_characters: #{e}"
end
```

#### Using the count_characters_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolCountCharactersResponse>, Integer, Hash)> count_characters_with_http_info(free_tool_count_characters_request)

```ruby
begin
  # Count characters as each network counts them
  data, status_code, headers = api_instance.count_characters_with_http_info(free_tool_count_characters_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolCountCharactersResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->count_characters_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_count_characters_request** | [**FreeToolCountCharactersRequest**](FreeToolCountCharactersRequest.md) |  |  |

### Return type

[**FreeToolCountCharactersResponse**](FreeToolCountCharactersResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## format_linked_in_post

> <FreeToolFormatLinkedInPostResponse> format_linked_in_post(free_tool_format_linked_in_post_request)

Format a LinkedIn post with bold, italic and lists

Format a LinkedIn post with bold, italic and lists. The same logic as the free web tool at https://postboost.co/tools/linkedin-post-formatter. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
free_tool_format_linked_in_post_request = PostBoost::FreeToolFormatLinkedInPostRequest.new({text: 'text_example'}) # FreeToolFormatLinkedInPostRequest | 

begin
  # Format a LinkedIn post with bold, italic and lists
  result = api_instance.format_linked_in_post(free_tool_format_linked_in_post_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->format_linked_in_post: #{e}"
end
```

#### Using the format_linked_in_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolFormatLinkedInPostResponse>, Integer, Hash)> format_linked_in_post_with_http_info(free_tool_format_linked_in_post_request)

```ruby
begin
  # Format a LinkedIn post with bold, italic and lists
  data, status_code, headers = api_instance.format_linked_in_post_with_http_info(free_tool_format_linked_in_post_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolFormatLinkedInPostResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->format_linked_in_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_format_linked_in_post_request** | [**FreeToolFormatLinkedInPostRequest**](FreeToolFormatLinkedInPostRequest.md) |  |  |

### Return type

[**FreeToolFormatLinkedInPostResponse**](FreeToolFormatLinkedInPostResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## generate_caption

> <FreeToolGenerateCaptionResponse> generate_caption(free_tool_generate_caption_request)

Write three post captions for a topic with AI (needs a token, spends AI credits)

Write three post captions for a topic with AI (needs a token, spends AI credits). The same logic as the free web tool at https://postboost.co/tools/instagram-caption-generator. Needs an API token (a scoped key needs the `ai` ability and pays with its own workspace). A new generation spends 1 AI credit of the workspace you name (or your active workspace); a repeated identical request is answered from the cache for free.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::FreeToolsApi.new
free_tool_generate_caption_request = PostBoost::FreeToolGenerateCaptionRequest.new({text: 'text_example'}) # FreeToolGenerateCaptionRequest | 

begin
  # Write three post captions for a topic with AI (needs a token, spends AI credits)
  result = api_instance.generate_caption(free_tool_generate_caption_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->generate_caption: #{e}"
end
```

#### Using the generate_caption_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolGenerateCaptionResponse>, Integer, Hash)> generate_caption_with_http_info(free_tool_generate_caption_request)

```ruby
begin
  # Write three post captions for a topic with AI (needs a token, spends AI credits)
  data, status_code, headers = api_instance.generate_caption_with_http_info(free_tool_generate_caption_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolGenerateCaptionResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->generate_caption_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_generate_caption_request** | [**FreeToolGenerateCaptionRequest**](FreeToolGenerateCaptionRequest.md) |  |  |

### Return type

[**FreeToolGenerateCaptionResponse**](FreeToolGenerateCaptionResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## generate_fancy_text

> <FreeToolGenerateFancyTextResponse> generate_fancy_text(free_tool_generate_fancy_text_request)

Convert text to fancy Unicode styles

Convert text to fancy Unicode styles. The same logic as the free web tool at https://postboost.co/tools/fancy-text-generator. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
free_tool_generate_fancy_text_request = PostBoost::FreeToolGenerateFancyTextRequest.new({text: 'text_example'}) # FreeToolGenerateFancyTextRequest | 

begin
  # Convert text to fancy Unicode styles
  result = api_instance.generate_fancy_text(free_tool_generate_fancy_text_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->generate_fancy_text: #{e}"
end
```

#### Using the generate_fancy_text_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolGenerateFancyTextResponse>, Integer, Hash)> generate_fancy_text_with_http_info(free_tool_generate_fancy_text_request)

```ruby
begin
  # Convert text to fancy Unicode styles
  data, status_code, headers = api_instance.generate_fancy_text_with_http_info(free_tool_generate_fancy_text_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolGenerateFancyTextResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->generate_fancy_text_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_generate_fancy_text_request** | [**FreeToolGenerateFancyTextRequest**](FreeToolGenerateFancyTextRequest.md) |  |  |

### Return type

[**FreeToolGenerateFancyTextResponse**](FreeToolGenerateFancyTextResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## generate_hashtags

> <FreeToolGenerateHashtagsResponse> generate_hashtags(free_tool_generate_hashtags_request)

Generate hashtags for a post topic with AI (needs a token, spends AI credits)

Generate hashtags for a post topic with AI (needs a token, spends AI credits). The same logic as the free web tool at https://postboost.co/tools/instagram-hashtag-generator. Needs an API token (a scoped key needs the `ai` ability and pays with its own workspace). A new generation spends 1 AI credit of the workspace you name (or your active workspace); a repeated identical request is answered from the cache for free.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::FreeToolsApi.new
free_tool_generate_hashtags_request = PostBoost::FreeToolGenerateHashtagsRequest.new({topic: 'topic_example'}) # FreeToolGenerateHashtagsRequest | 

begin
  # Generate hashtags for a post topic with AI (needs a token, spends AI credits)
  result = api_instance.generate_hashtags(free_tool_generate_hashtags_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->generate_hashtags: #{e}"
end
```

#### Using the generate_hashtags_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolGenerateHashtagsResponse>, Integer, Hash)> generate_hashtags_with_http_info(free_tool_generate_hashtags_request)

```ruby
begin
  # Generate hashtags for a post topic with AI (needs a token, spends AI credits)
  data, status_code, headers = api_instance.generate_hashtags_with_http_info(free_tool_generate_hashtags_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolGenerateHashtagsResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->generate_hashtags_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_generate_hashtags_request** | [**FreeToolGenerateHashtagsRequest**](FreeToolGenerateHashtagsRequest.md) |  |  |

### Return type

[**FreeToolGenerateHashtagsResponse**](FreeToolGenerateHashtagsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## get_best_times_to_post

> <FreeToolGetBestTimesToPostResponse> get_best_times_to_post(opts)

Get the best times to post per network from published studies, with sources

Get the best times to post per network from published studies, with sources. The same logic as the free web tool at https://postboost.co/tools/best-time-to-post. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
opts = {
  network: 'network_example' # String | 
}

begin
  # Get the best times to post per network from published studies, with sources
  result = api_instance.get_best_times_to_post(opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->get_best_times_to_post: #{e}"
end
```

#### Using the get_best_times_to_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolGetBestTimesToPostResponse>, Integer, Hash)> get_best_times_to_post_with_http_info(opts)

```ruby
begin
  # Get the best times to post per network from published studies, with sources
  data, status_code, headers = api_instance.get_best_times_to_post_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolGetBestTimesToPostResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->get_best_times_to_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **network** | **String** |  | [optional] |

### Return type

[**FreeToolGetBestTimesToPostResponse**](FreeToolGetBestTimesToPostResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_image_sizes

> <FreeToolGetImageSizesResponse> get_image_sizes(opts)

Get social media image sizes per network, each with its source

Get social media image sizes per network, each with its source. The same logic as the free web tool at https://postboost.co/tools/social-media-image-sizes. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
opts = {
  network: 'network_example' # String | 
}

begin
  # Get social media image sizes per network, each with its source
  result = api_instance.get_image_sizes(opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->get_image_sizes: #{e}"
end
```

#### Using the get_image_sizes_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolGetImageSizesResponse>, Integer, Hash)> get_image_sizes_with_http_info(opts)

```ruby
begin
  # Get social media image sizes per network, each with its source
  data, status_code, headers = api_instance.get_image_sizes_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolGetImageSizesResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->get_image_sizes_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **network** | **String** |  | [optional] |

### Return type

[**FreeToolGetImageSizesResponse**](FreeToolGetImageSizesResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_free_tools

> <FreeToolList> list_free_tools

List the free tools

Every free tool the API serves, with its operationId and web page. No token needed.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new

begin
  # List the free tools
  result = api_instance.list_free_tools
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->list_free_tools: #{e}"
end
```

#### Using the list_free_tools_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolList>, Integer, Hash)> list_free_tools_with_http_info

```ruby
begin
  # List the free tools
  data, status_code, headers = api_instance.list_free_tools_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolList>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->list_free_tools_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**FreeToolList**](FreeToolList.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## preview_post

> <FreeToolPreviewPostResponse> preview_post(free_tool_preview_post_request)

Preview where a post folds and when its image is cropped on Instagram, X, LinkedIn and Facebook

Preview where a post folds and when its image is cropped on Instagram, X, LinkedIn and Facebook. The same logic as the free web tool at https://postboost.co/tools/social-media-post-preview. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
free_tool_preview_post_request = PostBoost::FreeToolPreviewPostRequest.new({text: 'text_example'}) # FreeToolPreviewPostRequest | 

begin
  # Preview where a post folds and when its image is cropped on Instagram, X, LinkedIn and Facebook
  result = api_instance.preview_post(free_tool_preview_post_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->preview_post: #{e}"
end
```

#### Using the preview_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolPreviewPostResponse>, Integer, Hash)> preview_post_with_http_info(free_tool_preview_post_request)

```ruby
begin
  # Preview where a post folds and when its image is cropped on Instagram, X, LinkedIn and Facebook
  data, status_code, headers = api_instance.preview_post_with_http_info(free_tool_preview_post_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolPreviewPostResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->preview_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_preview_post_request** | [**FreeToolPreviewPostRequest**](FreeToolPreviewPostRequest.md) |  |  |

### Return type

[**FreeToolPreviewPostResponse**](FreeToolPreviewPostResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## split_thread

> <FreeToolSplitThreadResponse> split_thread(free_tool_split_thread_request)

Split long text into a thread

Split long text into a thread. The same logic as the free web tool at https://postboost.co/tools/x-thread-maker. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
free_tool_split_thread_request = PostBoost::FreeToolSplitThreadRequest.new # FreeToolSplitThreadRequest | 

begin
  # Split long text into a thread
  result = api_instance.split_thread(free_tool_split_thread_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->split_thread: #{e}"
end
```

#### Using the split_thread_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolSplitThreadResponse>, Integer, Hash)> split_thread_with_http_info(free_tool_split_thread_request)

```ruby
begin
  # Split long text into a thread
  data, status_code, headers = api_instance.split_thread_with_http_info(free_tool_split_thread_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolSplitThreadResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->split_thread_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_split_thread_request** | [**FreeToolSplitThreadRequest**](FreeToolSplitThreadRequest.md) |  |  |

### Return type

[**FreeToolSplitThreadResponse**](FreeToolSplitThreadResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

