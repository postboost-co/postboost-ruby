# PostBoost::AIApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**blog_to_social**](AIApi.md#blog_to_social) | **POST** /{workspaceUuid}/ai/blog-to-social | Generate social media captions from a blog post |


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

