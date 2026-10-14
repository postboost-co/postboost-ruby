# PostBoost::FreeToolsApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**build_utm_url**](FreeToolsApi.md#build_utm_url) | **POST** /tools/utm-builder | Build a UTM-tagged campaign URL |
| [**calculate_engagement_rate**](FreeToolsApi.md#calculate_engagement_rate) | **POST** /tools/engagement-rate-calculator | Calculate an engagement rate |
| [**count_characters**](FreeToolsApi.md#count_characters) | **POST** /tools/social-media-character-counter | Count characters as each network counts them |
| [**format_linked_in_post**](FreeToolsApi.md#format_linked_in_post) | **POST** /tools/linkedin-post-formatter | Format a LinkedIn post with bold, italic and lists |
| [**generate_fancy_text**](FreeToolsApi.md#generate_fancy_text) | **POST** /tools/fancy-text-generator | Convert text to fancy Unicode styles |
| [**list_free_tools**](FreeToolsApi.md#list_free_tools) | **GET** /tools | List the free tools |
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

