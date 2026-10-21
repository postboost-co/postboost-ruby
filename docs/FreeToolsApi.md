# PostBoost::FreeToolsApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**build_hashtag_groups**](FreeToolsApi.md#build_hashtag_groups) | **POST** /tools/hashtag-group-builder | Clean, dedupe and split hashtags into groups that fit a network&#39;s hashtag cap |
| [**build_utm_url**](FreeToolsApi.md#build_utm_url) | **POST** /tools/utm-builder | Build a UTM-tagged campaign URL |
| [**calculate_aspect_ratio**](FreeToolsApi.md#calculate_aspect_ratio) | **POST** /tools/aspect-ratio-calculator | Calculate an aspect ratio, or the missing side of an image at a given ratio |
| [**calculate_carousel_slices**](FreeToolsApi.md#calculate_carousel_slices) | **POST** /tools/instagram-carousel-splitter | Split a wide image into seamless Instagram carousel slides |
| [**calculate_crop**](FreeToolsApi.md#calculate_crop) | **POST** /tools/social-media-image-sizes/crop | Calculate the crop box that fits an image to a social media size |
| [**calculate_engagement_rate**](FreeToolsApi.md#calculate_engagement_rate) | **POST** /tools/engagement-rate-calculator | Calculate an engagement rate |
| [**calculate_influencer_rate**](FreeToolsApi.md#calculate_influencer_rate) | **POST** /tools/influencer-rate-calculator | Estimate an influencer&#39;s rate for one sponsored deliverable |
| [**calculate_smm_pricing**](FreeToolsApi.md#calculate_smm_pricing) | **POST** /tools/social-media-manager-pricing-calculator | Estimate social media manager pricing |
| [**calculate_social_roi**](FreeToolsApi.md#calculate_social_roi) | **POST** /tools/social-media-roi-calculator | Calculate social media ROI |
| [**calculate_x_api_cost**](FreeToolsApi.md#calculate_x_api_cost) | **POST** /tools/x-api-cost-calculator | Calculate the monthly X API cost |
| [**check_link_preview**](FreeToolsApi.md#check_link_preview) | **POST** /tools/link-preview-checker | Check how a link previews on X, LinkedIn, Facebook and chat apps (Open Graph and Twitter card tags) |
| [**check_post**](FreeToolsApi.md#check_post) | **POST** /tools/social-media-post-checker | Check a post against each network&#39;s publishing rules |
| [**check_readability**](FreeToolsApi.md#check_readability) | **POST** /tools/post-readability-checker | Check the readability of a post: Flesch scores, long sentences and passive hints |
| [**check_youtube_thumbnail**](FreeToolsApi.md#check_youtube_thumbnail) | **POST** /tools/youtube-thumbnail-size-checker | Check a YouTube thumbnail&#39;s ratio, width, file size and format against YouTube&#39;s requirements |
| [**clean_text**](FreeToolsApi.md#clean_text) | **POST** /tools/ai-text-cleaner | Clean AI-written text: dashes, quotes, invisible characters, markdown |
| [**count_characters**](FreeToolsApi.md#count_characters) | **POST** /tools/social-media-character-counter | Count characters as each network counts them |
| [**find_automation_recipes**](FreeToolsApi.md#find_automation_recipes) | **GET** /tools/social-media-automation-recipes | Find n8n, Zapier and Make recipes that automate social media posting through the PostBoost API |
| [**format_cross_post**](FreeToolsApi.md#format_cross_post) | **POST** /tools/cross-post-formatter | Format one post for X, Threads, Bluesky, Mastodon and LinkedIn |
| [**format_instagram_caption**](FreeToolsApi.md#format_instagram_caption) | **POST** /tools/instagram-line-break-generator | Keep blank lines in an Instagram caption with spacer lines, and count it |
| [**format_linked_in_post**](FreeToolsApi.md#format_linked_in_post) | **POST** /tools/linkedin-post-formatter | Format a LinkedIn post with bold, italic and lists |
| [**generate_alt_text**](FreeToolsApi.md#generate_alt_text) | **POST** /tools/alt-text-generator | Write alt text for an image with AI (needs a token, spends AI credits) |
| [**generate_bio**](FreeToolsApi.md#generate_bio) | **POST** /tools/instagram-bio-generator | Write five profile bios with AI (needs a token, spends AI credits) |
| [**generate_caption**](FreeToolsApi.md#generate_caption) | **POST** /tools/instagram-caption-generator | Write three post captions for a topic with AI (needs a token, spends AI credits) |
| [**generate_fancy_text**](FreeToolsApi.md#generate_fancy_text) | **POST** /tools/fancy-text-generator | Convert text to fancy Unicode styles |
| [**generate_hashtags**](FreeToolsApi.md#generate_hashtags) | **POST** /tools/instagram-hashtag-generator | Generate hashtags for a post topic with AI (needs a token, spends AI credits) |
| [**generate_hooks**](FreeToolsApi.md#generate_hooks) | **POST** /tools/hook-generator | Generate hooks (opening lines) for a social media post with AI (needs a token, spends AI credits) |
| [**generate_linked_in_headline**](FreeToolsApi.md#generate_linked_in_headline) | **POST** /tools/linkedin-headline-generator | Write five LinkedIn profile headlines with AI (needs a token, spends AI credits) |
| [**generate_qr_code**](FreeToolsApi.md#generate_qr_code) | **POST** /tools/qr-code-generator | Generate a QR code (SVG) for a link or text, with optional UTM tags |
| [**generate_social_posts_from_blog**](FreeToolsApi.md#generate_social_posts_from_blog) | **POST** /tools/blog-to-social-media | Turn a blog post (URL or text) into one social post per network with AI (needs a token, spends AI credits) |
| [**generate_usernames**](FreeToolsApi.md#generate_usernames) | **POST** /tools/social-media-username-generator | Generate social media usernames |
| [**generate_youtube_description**](FreeToolsApi.md#generate_youtube_description) | **POST** /tools/youtube-description-generator | Write three YouTube video descriptions with AI (needs a token, spends AI credits) |
| [**generate_youtube_titles**](FreeToolsApi.md#generate_youtube_titles) | **POST** /tools/youtube-title-generator | Write five YouTube video titles with AI (needs a token, spends AI credits) |
| [**get_best_times_to_post**](FreeToolsApi.md#get_best_times_to_post) | **GET** /tools/best-time-to-post | Get the best times to post per network from published studies, with sources |
| [**get_glossary**](FreeToolsApi.md#get_glossary) | **GET** /tools/social-media-glossary | Look up social media terms: plain-language definitions by category, with sources and related terms |
| [**get_hook_templates**](FreeToolsApi.md#get_hook_templates) | **GET** /tools/hook-generator/library | Get free hook templates for social media posts, filtered by style and network |
| [**get_image_sizes**](FreeToolsApi.md#get_image_sizes) | **GET** /tools/social-media-image-sizes | Get social media image sizes per network, each with its source |
| [**get_safe_zones**](FreeToolsApi.md#get_safe_zones) | **POST** /tools/safe-zone-checker | Get the TikTok, Instagram Reels or YouTube Shorts safe zones for a vertical frame |
| [**get_video_specs**](FreeToolsApi.md#get_video_specs) | **GET** /tools/social-media-video-specs | Get social media video ratios, resolutions, lengths and file size limits per network, with sources |
| [**list_awareness_days**](FreeToolsApi.md#list_awareness_days) | **GET** /tools/social-media-holiday-calendar | List public holidays, awareness days and social media days by date, country, type and topic, with sources |
| [**list_free_tools**](FreeToolsApi.md#list_free_tools) | **GET** /tools | List the free tools |
| [**pick_giveaway_winners**](FreeToolsApi.md#pick_giveaway_winners) | **POST** /tools/giveaway-comment-picker | Pick giveaway winners with a draw anyone can verify |
| [**pick_social_media_tool**](FreeToolsApi.md#pick_social_media_tool) | **POST** /tools/social-media-tool-picker | Match your needs against social media management tools and see what each one misses |
| [**plan_content_calendar**](FreeToolsApi.md#plan_content_calendar) | **POST** /tools/social-media-content-calendar-generator | Plan a social media content calendar and get it as CSV and ICS |
| [**plan_posting_frequency**](FreeToolsApi.md#plan_posting_frequency) | **POST** /tools/posting-frequency-planner | Plan how often to post on each network |
| [**preview_post**](FreeToolsApi.md#preview_post) | **POST** /tools/social-media-post-preview | Preview where a post folds and when its image is cropped on Instagram, X, LinkedIn and Facebook |
| [**score_social_audit**](FreeToolsApi.md#score_social_audit) | **POST** /tools/social-media-audit-template | Score a social media audit checklist and get the top fixes |
| [**search_emoji**](FreeToolsApi.md#search_emoji) | **POST** /tools/social-media-emoji-picker | Search emoji by name or keyword, to copy and paste into a post |
| [**split_thread**](FreeToolsApi.md#split_thread) | **POST** /tools/x-thread-maker | Split long text into a thread |
| [**summarize_report**](FreeToolsApi.md#summarize_report) | **POST** /tools/social-media-report-generator | Summarize social media post metrics into a report |
| [**verify_webhook_signature**](FreeToolsApi.md#verify_webhook_signature) | **POST** /tools/webhook-signature-verifier | Verify an HMAC webhook signature |


## build_hashtag_groups

> <FreeToolBuildHashtagGroupsResponse> build_hashtag_groups(free_tool_build_hashtag_groups_request)

Clean, dedupe and split hashtags into groups that fit a network's hashtag cap

Clean, dedupe and split hashtags into groups that fit a network's hashtag cap. The same logic as the free web tool at https://postboost.co/tools/hashtag-group-builder. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
free_tool_build_hashtag_groups_request = PostBoost::FreeToolBuildHashtagGroupsRequest.new({text: 'text_example'}) # FreeToolBuildHashtagGroupsRequest | 

begin
  # Clean, dedupe and split hashtags into groups that fit a network's hashtag cap
  result = api_instance.build_hashtag_groups(free_tool_build_hashtag_groups_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->build_hashtag_groups: #{e}"
end
```

#### Using the build_hashtag_groups_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolBuildHashtagGroupsResponse>, Integer, Hash)> build_hashtag_groups_with_http_info(free_tool_build_hashtag_groups_request)

```ruby
begin
  # Clean, dedupe and split hashtags into groups that fit a network's hashtag cap
  data, status_code, headers = api_instance.build_hashtag_groups_with_http_info(free_tool_build_hashtag_groups_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolBuildHashtagGroupsResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->build_hashtag_groups_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_build_hashtag_groups_request** | [**FreeToolBuildHashtagGroupsRequest**](FreeToolBuildHashtagGroupsRequest.md) |  |  |

### Return type

[**FreeToolBuildHashtagGroupsResponse**](FreeToolBuildHashtagGroupsResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


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


## calculate_carousel_slices

> <FreeToolCalculateCarouselSlicesResponse> calculate_carousel_slices(free_tool_calculate_carousel_slices_request)

Split a wide image into seamless Instagram carousel slides

Split a wide image into seamless Instagram carousel slides. The same logic as the free web tool at https://postboost.co/tools/instagram-carousel-splitter. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
free_tool_calculate_carousel_slices_request = PostBoost::FreeToolCalculateCarouselSlicesRequest.new({width: 37, height: 37, slides: 37}) # FreeToolCalculateCarouselSlicesRequest | 

begin
  # Split a wide image into seamless Instagram carousel slides
  result = api_instance.calculate_carousel_slices(free_tool_calculate_carousel_slices_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->calculate_carousel_slices: #{e}"
end
```

#### Using the calculate_carousel_slices_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolCalculateCarouselSlicesResponse>, Integer, Hash)> calculate_carousel_slices_with_http_info(free_tool_calculate_carousel_slices_request)

```ruby
begin
  # Split a wide image into seamless Instagram carousel slides
  data, status_code, headers = api_instance.calculate_carousel_slices_with_http_info(free_tool_calculate_carousel_slices_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolCalculateCarouselSlicesResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->calculate_carousel_slices_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_calculate_carousel_slices_request** | [**FreeToolCalculateCarouselSlicesRequest**](FreeToolCalculateCarouselSlicesRequest.md) |  |  |

### Return type

[**FreeToolCalculateCarouselSlicesResponse**](FreeToolCalculateCarouselSlicesResponse.md)

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


## calculate_influencer_rate

> <FreeToolCalculateInfluencerRateResponse> calculate_influencer_rate(free_tool_calculate_influencer_rate_request)

Estimate an influencer's rate for one sponsored deliverable

Estimate an influencer's rate for one sponsored deliverable. The same logic as the free web tool at https://postboost.co/tools/influencer-rate-calculator. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
free_tool_calculate_influencer_rate_request = PostBoost::FreeToolCalculateInfluencerRateRequest.new({network: 'instagram', followers: 37}) # FreeToolCalculateInfluencerRateRequest | 

begin
  # Estimate an influencer's rate for one sponsored deliverable
  result = api_instance.calculate_influencer_rate(free_tool_calculate_influencer_rate_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->calculate_influencer_rate: #{e}"
end
```

#### Using the calculate_influencer_rate_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolCalculateInfluencerRateResponse>, Integer, Hash)> calculate_influencer_rate_with_http_info(free_tool_calculate_influencer_rate_request)

```ruby
begin
  # Estimate an influencer's rate for one sponsored deliverable
  data, status_code, headers = api_instance.calculate_influencer_rate_with_http_info(free_tool_calculate_influencer_rate_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolCalculateInfluencerRateResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->calculate_influencer_rate_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_calculate_influencer_rate_request** | [**FreeToolCalculateInfluencerRateRequest**](FreeToolCalculateInfluencerRateRequest.md) |  |  |

### Return type

[**FreeToolCalculateInfluencerRateResponse**](FreeToolCalculateInfluencerRateResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## calculate_smm_pricing

> <FreeToolCalculateSmmPricingResponse> calculate_smm_pricing(free_tool_calculate_smm_pricing_request)

Estimate social media manager pricing

Estimate social media manager pricing. The same logic as the free web tool at https://postboost.co/tools/social-media-manager-pricing-calculator. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
free_tool_calculate_smm_pricing_request = PostBoost::FreeToolCalculateSmmPricingRequest.new({networks: 37, posts_per_week: 37}) # FreeToolCalculateSmmPricingRequest | 

begin
  # Estimate social media manager pricing
  result = api_instance.calculate_smm_pricing(free_tool_calculate_smm_pricing_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->calculate_smm_pricing: #{e}"
end
```

#### Using the calculate_smm_pricing_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolCalculateSmmPricingResponse>, Integer, Hash)> calculate_smm_pricing_with_http_info(free_tool_calculate_smm_pricing_request)

```ruby
begin
  # Estimate social media manager pricing
  data, status_code, headers = api_instance.calculate_smm_pricing_with_http_info(free_tool_calculate_smm_pricing_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolCalculateSmmPricingResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->calculate_smm_pricing_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_calculate_smm_pricing_request** | [**FreeToolCalculateSmmPricingRequest**](FreeToolCalculateSmmPricingRequest.md) |  |  |

### Return type

[**FreeToolCalculateSmmPricingResponse**](FreeToolCalculateSmmPricingResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## calculate_social_roi

> <FreeToolCalculateSocialRoiResponse> calculate_social_roi(free_tool_calculate_social_roi_request)

Calculate social media ROI

Calculate social media ROI. The same logic as the free web tool at https://postboost.co/tools/social-media-roi-calculator. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
free_tool_calculate_social_roi_request = PostBoost::FreeToolCalculateSocialRoiRequest.new({revenue: 3.56}) # FreeToolCalculateSocialRoiRequest | 

begin
  # Calculate social media ROI
  result = api_instance.calculate_social_roi(free_tool_calculate_social_roi_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->calculate_social_roi: #{e}"
end
```

#### Using the calculate_social_roi_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolCalculateSocialRoiResponse>, Integer, Hash)> calculate_social_roi_with_http_info(free_tool_calculate_social_roi_request)

```ruby
begin
  # Calculate social media ROI
  data, status_code, headers = api_instance.calculate_social_roi_with_http_info(free_tool_calculate_social_roi_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolCalculateSocialRoiResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->calculate_social_roi_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_calculate_social_roi_request** | [**FreeToolCalculateSocialRoiRequest**](FreeToolCalculateSocialRoiRequest.md) |  |  |

### Return type

[**FreeToolCalculateSocialRoiResponse**](FreeToolCalculateSocialRoiResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## calculate_x_api_cost

> <FreeToolCalculateXApiCostResponse> calculate_x_api_cost(free_tool_calculate_x_api_cost_request)

Calculate the monthly X API cost

Calculate the monthly X API cost. The same logic as the free web tool at https://postboost.co/tools/x-api-cost-calculator. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
free_tool_calculate_x_api_cost_request = PostBoost::FreeToolCalculateXApiCostRequest.new # FreeToolCalculateXApiCostRequest | 

begin
  # Calculate the monthly X API cost
  result = api_instance.calculate_x_api_cost(free_tool_calculate_x_api_cost_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->calculate_x_api_cost: #{e}"
end
```

#### Using the calculate_x_api_cost_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolCalculateXApiCostResponse>, Integer, Hash)> calculate_x_api_cost_with_http_info(free_tool_calculate_x_api_cost_request)

```ruby
begin
  # Calculate the monthly X API cost
  data, status_code, headers = api_instance.calculate_x_api_cost_with_http_info(free_tool_calculate_x_api_cost_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolCalculateXApiCostResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->calculate_x_api_cost_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_calculate_x_api_cost_request** | [**FreeToolCalculateXApiCostRequest**](FreeToolCalculateXApiCostRequest.md) |  |  |

### Return type

[**FreeToolCalculateXApiCostResponse**](FreeToolCalculateXApiCostResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## check_link_preview

> <FreeToolCheckLinkPreviewResponse> check_link_preview(free_tool_check_link_preview_request)

Check how a link previews on X, LinkedIn, Facebook and chat apps (Open Graph and Twitter card tags)

Check how a link previews on X, LinkedIn, Facebook and chat apps (Open Graph and Twitter card tags). The same logic as the free web tool at https://postboost.co/tools/link-preview-checker. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
free_tool_check_link_preview_request = PostBoost::FreeToolCheckLinkPreviewRequest.new({url: 'url_example'}) # FreeToolCheckLinkPreviewRequest | 

begin
  # Check how a link previews on X, LinkedIn, Facebook and chat apps (Open Graph and Twitter card tags)
  result = api_instance.check_link_preview(free_tool_check_link_preview_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->check_link_preview: #{e}"
end
```

#### Using the check_link_preview_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolCheckLinkPreviewResponse>, Integer, Hash)> check_link_preview_with_http_info(free_tool_check_link_preview_request)

```ruby
begin
  # Check how a link previews on X, LinkedIn, Facebook and chat apps (Open Graph and Twitter card tags)
  data, status_code, headers = api_instance.check_link_preview_with_http_info(free_tool_check_link_preview_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolCheckLinkPreviewResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->check_link_preview_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_check_link_preview_request** | [**FreeToolCheckLinkPreviewRequest**](FreeToolCheckLinkPreviewRequest.md) |  |  |

### Return type

[**FreeToolCheckLinkPreviewResponse**](FreeToolCheckLinkPreviewResponse.md)

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


## check_readability

> <FreeToolCheckReadabilityResponse> check_readability(free_tool_check_readability_request)

Check the readability of a post: Flesch scores, long sentences and passive hints

Check the readability of a post: Flesch scores, long sentences and passive hints. The same logic as the free web tool at https://postboost.co/tools/post-readability-checker. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
free_tool_check_readability_request = PostBoost::FreeToolCheckReadabilityRequest.new({text: 'text_example'}) # FreeToolCheckReadabilityRequest | 

begin
  # Check the readability of a post: Flesch scores, long sentences and passive hints
  result = api_instance.check_readability(free_tool_check_readability_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->check_readability: #{e}"
end
```

#### Using the check_readability_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolCheckReadabilityResponse>, Integer, Hash)> check_readability_with_http_info(free_tool_check_readability_request)

```ruby
begin
  # Check the readability of a post: Flesch scores, long sentences and passive hints
  data, status_code, headers = api_instance.check_readability_with_http_info(free_tool_check_readability_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolCheckReadabilityResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->check_readability_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_check_readability_request** | [**FreeToolCheckReadabilityRequest**](FreeToolCheckReadabilityRequest.md) |  |  |

### Return type

[**FreeToolCheckReadabilityResponse**](FreeToolCheckReadabilityResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## check_youtube_thumbnail

> <FreeToolCheckYoutubeThumbnailResponse> check_youtube_thumbnail(free_tool_check_youtube_thumbnail_request)

Check a YouTube thumbnail's ratio, width, file size and format against YouTube's requirements

Check a YouTube thumbnail's ratio, width, file size and format against YouTube's requirements. The same logic as the free web tool at https://postboost.co/tools/youtube-thumbnail-size-checker. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
free_tool_check_youtube_thumbnail_request = PostBoost::FreeToolCheckYoutubeThumbnailRequest.new({width: 37, height: 37, file_size_bytes: 37, format: 'format_example'}) # FreeToolCheckYoutubeThumbnailRequest | 

begin
  # Check a YouTube thumbnail's ratio, width, file size and format against YouTube's requirements
  result = api_instance.check_youtube_thumbnail(free_tool_check_youtube_thumbnail_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->check_youtube_thumbnail: #{e}"
end
```

#### Using the check_youtube_thumbnail_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolCheckYoutubeThumbnailResponse>, Integer, Hash)> check_youtube_thumbnail_with_http_info(free_tool_check_youtube_thumbnail_request)

```ruby
begin
  # Check a YouTube thumbnail's ratio, width, file size and format against YouTube's requirements
  data, status_code, headers = api_instance.check_youtube_thumbnail_with_http_info(free_tool_check_youtube_thumbnail_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolCheckYoutubeThumbnailResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->check_youtube_thumbnail_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_check_youtube_thumbnail_request** | [**FreeToolCheckYoutubeThumbnailRequest**](FreeToolCheckYoutubeThumbnailRequest.md) |  |  |

### Return type

[**FreeToolCheckYoutubeThumbnailResponse**](FreeToolCheckYoutubeThumbnailResponse.md)

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


## find_automation_recipes

> <FreeToolFindAutomationRecipesResponse> find_automation_recipes(opts)

Find n8n, Zapier and Make recipes that automate social media posting through the PostBoost API

Find n8n, Zapier and Make recipes that automate social media posting through the PostBoost API. The same logic as the free web tool at https://postboost.co/tools/social-media-automation-recipes. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
opts = {
  platform: 'n8n', # String | 
  trigger: 'rss', # String | 
  q: 'q_example' # String | 
}

begin
  # Find n8n, Zapier and Make recipes that automate social media posting through the PostBoost API
  result = api_instance.find_automation_recipes(opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->find_automation_recipes: #{e}"
end
```

#### Using the find_automation_recipes_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolFindAutomationRecipesResponse>, Integer, Hash)> find_automation_recipes_with_http_info(opts)

```ruby
begin
  # Find n8n, Zapier and Make recipes that automate social media posting through the PostBoost API
  data, status_code, headers = api_instance.find_automation_recipes_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolFindAutomationRecipesResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->find_automation_recipes_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **platform** | **String** |  | [optional] |
| **trigger** | **String** |  | [optional] |
| **q** | **String** |  | [optional] |

### Return type

[**FreeToolFindAutomationRecipesResponse**](FreeToolFindAutomationRecipesResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## format_cross_post

> <FreeToolFormatCrossPostResponse> format_cross_post(free_tool_format_cross_post_request)

Format one post for X, Threads, Bluesky, Mastodon and LinkedIn

Format one post for X, Threads, Bluesky, Mastodon and LinkedIn. The same logic as the free web tool at https://postboost.co/tools/cross-post-formatter. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
free_tool_format_cross_post_request = PostBoost::FreeToolFormatCrossPostRequest.new # FreeToolFormatCrossPostRequest | 

begin
  # Format one post for X, Threads, Bluesky, Mastodon and LinkedIn
  result = api_instance.format_cross_post(free_tool_format_cross_post_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->format_cross_post: #{e}"
end
```

#### Using the format_cross_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolFormatCrossPostResponse>, Integer, Hash)> format_cross_post_with_http_info(free_tool_format_cross_post_request)

```ruby
begin
  # Format one post for X, Threads, Bluesky, Mastodon and LinkedIn
  data, status_code, headers = api_instance.format_cross_post_with_http_info(free_tool_format_cross_post_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolFormatCrossPostResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->format_cross_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_format_cross_post_request** | [**FreeToolFormatCrossPostRequest**](FreeToolFormatCrossPostRequest.md) |  |  |

### Return type

[**FreeToolFormatCrossPostResponse**](FreeToolFormatCrossPostResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## format_instagram_caption

> <FreeToolFormatInstagramCaptionResponse> format_instagram_caption(free_tool_format_instagram_caption_request)

Keep blank lines in an Instagram caption with spacer lines, and count it

Keep blank lines in an Instagram caption with spacer lines, and count it. The same logic as the free web tool at https://postboost.co/tools/instagram-line-break-generator. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
free_tool_format_instagram_caption_request = PostBoost::FreeToolFormatInstagramCaptionRequest.new({text: 'text_example'}) # FreeToolFormatInstagramCaptionRequest | 

begin
  # Keep blank lines in an Instagram caption with spacer lines, and count it
  result = api_instance.format_instagram_caption(free_tool_format_instagram_caption_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->format_instagram_caption: #{e}"
end
```

#### Using the format_instagram_caption_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolFormatInstagramCaptionResponse>, Integer, Hash)> format_instagram_caption_with_http_info(free_tool_format_instagram_caption_request)

```ruby
begin
  # Keep blank lines in an Instagram caption with spacer lines, and count it
  data, status_code, headers = api_instance.format_instagram_caption_with_http_info(free_tool_format_instagram_caption_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolFormatInstagramCaptionResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->format_instagram_caption_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_format_instagram_caption_request** | [**FreeToolFormatInstagramCaptionRequest**](FreeToolFormatInstagramCaptionRequest.md) |  |  |

### Return type

[**FreeToolFormatInstagramCaptionResponse**](FreeToolFormatInstagramCaptionResponse.md)

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


## generate_alt_text

> <FreeToolGenerateAltTextResponse> generate_alt_text(free_tool_generate_alt_text_request)

Write alt text for an image with AI (needs a token, spends AI credits)

Write alt text for an image with AI (needs a token, spends AI credits). The same logic as the free web tool at https://postboost.co/tools/alt-text-generator. Needs an API token (a scoped key needs the `ai` ability and pays with its own workspace). A new generation spends 1 AI credit of the workspace you name (or your active workspace); a repeated identical request is answered from the cache for free.

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
free_tool_generate_alt_text_request = PostBoost::FreeToolGenerateAltTextRequest.new # FreeToolGenerateAltTextRequest | 

begin
  # Write alt text for an image with AI (needs a token, spends AI credits)
  result = api_instance.generate_alt_text(free_tool_generate_alt_text_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->generate_alt_text: #{e}"
end
```

#### Using the generate_alt_text_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolGenerateAltTextResponse>, Integer, Hash)> generate_alt_text_with_http_info(free_tool_generate_alt_text_request)

```ruby
begin
  # Write alt text for an image with AI (needs a token, spends AI credits)
  data, status_code, headers = api_instance.generate_alt_text_with_http_info(free_tool_generate_alt_text_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolGenerateAltTextResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->generate_alt_text_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_generate_alt_text_request** | [**FreeToolGenerateAltTextRequest**](FreeToolGenerateAltTextRequest.md) |  |  |

### Return type

[**FreeToolGenerateAltTextResponse**](FreeToolGenerateAltTextResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json, multipart/form-data
- **Accept**: application/json


## generate_bio

> <FreeToolGenerateBioResponse> generate_bio(free_tool_generate_bio_request)

Write five profile bios with AI (needs a token, spends AI credits)

Write five profile bios with AI (needs a token, spends AI credits). The same logic as the free web tool at https://postboost.co/tools/instagram-bio-generator. Needs an API token (a scoped key needs the `ai` ability and pays with its own workspace). A new generation spends 1 AI credit of the workspace you name (or your active workspace); a repeated identical request is answered from the cache for free.

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
free_tool_generate_bio_request = PostBoost::FreeToolGenerateBioRequest.new({text: 'text_example'}) # FreeToolGenerateBioRequest | 

begin
  # Write five profile bios with AI (needs a token, spends AI credits)
  result = api_instance.generate_bio(free_tool_generate_bio_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->generate_bio: #{e}"
end
```

#### Using the generate_bio_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolGenerateBioResponse>, Integer, Hash)> generate_bio_with_http_info(free_tool_generate_bio_request)

```ruby
begin
  # Write five profile bios with AI (needs a token, spends AI credits)
  data, status_code, headers = api_instance.generate_bio_with_http_info(free_tool_generate_bio_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolGenerateBioResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->generate_bio_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_generate_bio_request** | [**FreeToolGenerateBioRequest**](FreeToolGenerateBioRequest.md) |  |  |

### Return type

[**FreeToolGenerateBioResponse**](FreeToolGenerateBioResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

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


## generate_hooks

> <FreeToolGenerateHooksResponse> generate_hooks(free_tool_generate_hooks_request)

Generate hooks (opening lines) for a social media post with AI (needs a token, spends AI credits)

Generate hooks (opening lines) for a social media post with AI (needs a token, spends AI credits). The same logic as the free web tool at https://postboost.co/tools/hook-generator. Needs an API token (a scoped key needs the `ai` ability and pays with its own workspace). A new generation spends 1 AI credit of the workspace you name (or your active workspace); a repeated identical request is answered from the cache for free.

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
free_tool_generate_hooks_request = PostBoost::FreeToolGenerateHooksRequest.new({topic: 'topic_example'}) # FreeToolGenerateHooksRequest | 

begin
  # Generate hooks (opening lines) for a social media post with AI (needs a token, spends AI credits)
  result = api_instance.generate_hooks(free_tool_generate_hooks_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->generate_hooks: #{e}"
end
```

#### Using the generate_hooks_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolGenerateHooksResponse>, Integer, Hash)> generate_hooks_with_http_info(free_tool_generate_hooks_request)

```ruby
begin
  # Generate hooks (opening lines) for a social media post with AI (needs a token, spends AI credits)
  data, status_code, headers = api_instance.generate_hooks_with_http_info(free_tool_generate_hooks_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolGenerateHooksResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->generate_hooks_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_generate_hooks_request** | [**FreeToolGenerateHooksRequest**](FreeToolGenerateHooksRequest.md) |  |  |

### Return type

[**FreeToolGenerateHooksResponse**](FreeToolGenerateHooksResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## generate_linked_in_headline

> <FreeToolGenerateLinkedInHeadlineResponse> generate_linked_in_headline(free_tool_generate_linked_in_headline_request)

Write five LinkedIn profile headlines with AI (needs a token, spends AI credits)

Write five LinkedIn profile headlines with AI (needs a token, spends AI credits). The same logic as the free web tool at https://postboost.co/tools/linkedin-headline-generator. Needs an API token (a scoped key needs the `ai` ability and pays with its own workspace). A new generation spends 1 AI credit of the workspace you name (or your active workspace); a repeated identical request is answered from the cache for free.

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
free_tool_generate_linked_in_headline_request = PostBoost::FreeToolGenerateLinkedInHeadlineRequest.new({role: 'role_example', skills: 'skills_example'}) # FreeToolGenerateLinkedInHeadlineRequest | 

begin
  # Write five LinkedIn profile headlines with AI (needs a token, spends AI credits)
  result = api_instance.generate_linked_in_headline(free_tool_generate_linked_in_headline_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->generate_linked_in_headline: #{e}"
end
```

#### Using the generate_linked_in_headline_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolGenerateLinkedInHeadlineResponse>, Integer, Hash)> generate_linked_in_headline_with_http_info(free_tool_generate_linked_in_headline_request)

```ruby
begin
  # Write five LinkedIn profile headlines with AI (needs a token, spends AI credits)
  data, status_code, headers = api_instance.generate_linked_in_headline_with_http_info(free_tool_generate_linked_in_headline_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolGenerateLinkedInHeadlineResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->generate_linked_in_headline_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_generate_linked_in_headline_request** | [**FreeToolGenerateLinkedInHeadlineRequest**](FreeToolGenerateLinkedInHeadlineRequest.md) |  |  |

### Return type

[**FreeToolGenerateLinkedInHeadlineResponse**](FreeToolGenerateLinkedInHeadlineResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## generate_qr_code

> <FreeToolGenerateQrCodeResponse> generate_qr_code(free_tool_generate_qr_code_request)

Generate a QR code (SVG) for a link or text, with optional UTM tags

Generate a QR code (SVG) for a link or text, with optional UTM tags. The same logic as the free web tool at https://postboost.co/tools/qr-code-generator. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
free_tool_generate_qr_code_request = PostBoost::FreeToolGenerateQrCodeRequest.new({data: 'data_example'}) # FreeToolGenerateQrCodeRequest | 

begin
  # Generate a QR code (SVG) for a link or text, with optional UTM tags
  result = api_instance.generate_qr_code(free_tool_generate_qr_code_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->generate_qr_code: #{e}"
end
```

#### Using the generate_qr_code_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolGenerateQrCodeResponse>, Integer, Hash)> generate_qr_code_with_http_info(free_tool_generate_qr_code_request)

```ruby
begin
  # Generate a QR code (SVG) for a link or text, with optional UTM tags
  data, status_code, headers = api_instance.generate_qr_code_with_http_info(free_tool_generate_qr_code_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolGenerateQrCodeResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->generate_qr_code_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_generate_qr_code_request** | [**FreeToolGenerateQrCodeRequest**](FreeToolGenerateQrCodeRequest.md) |  |  |

### Return type

[**FreeToolGenerateQrCodeResponse**](FreeToolGenerateQrCodeResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## generate_social_posts_from_blog

> <FreeToolGenerateSocialPostsFromBlogResponse> generate_social_posts_from_blog(free_tool_generate_social_posts_from_blog_request)

Turn a blog post (URL or text) into one social post per network with AI (needs a token, spends AI credits)

Turn a blog post (URL or text) into one social post per network with AI (needs a token, spends AI credits). The same logic as the free web tool at https://postboost.co/tools/blog-to-social-media. Needs an API token (a scoped key needs the `ai` ability and pays with its own workspace). Each post spends 1 AI credit of the workspace you name (or your active workspace), so a call costs one credit per platform that comes back; results are not cached.

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
free_tool_generate_social_posts_from_blog_request = PostBoost::FreeToolGenerateSocialPostsFromBlogRequest.new({platforms: ['facebook']}) # FreeToolGenerateSocialPostsFromBlogRequest | 

begin
  # Turn a blog post (URL or text) into one social post per network with AI (needs a token, spends AI credits)
  result = api_instance.generate_social_posts_from_blog(free_tool_generate_social_posts_from_blog_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->generate_social_posts_from_blog: #{e}"
end
```

#### Using the generate_social_posts_from_blog_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolGenerateSocialPostsFromBlogResponse>, Integer, Hash)> generate_social_posts_from_blog_with_http_info(free_tool_generate_social_posts_from_blog_request)

```ruby
begin
  # Turn a blog post (URL or text) into one social post per network with AI (needs a token, spends AI credits)
  data, status_code, headers = api_instance.generate_social_posts_from_blog_with_http_info(free_tool_generate_social_posts_from_blog_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolGenerateSocialPostsFromBlogResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->generate_social_posts_from_blog_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_generate_social_posts_from_blog_request** | [**FreeToolGenerateSocialPostsFromBlogRequest**](FreeToolGenerateSocialPostsFromBlogRequest.md) |  |  |

### Return type

[**FreeToolGenerateSocialPostsFromBlogResponse**](FreeToolGenerateSocialPostsFromBlogResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## generate_usernames

> <FreeToolGenerateUsernamesResponse> generate_usernames(free_tool_generate_usernames_request)

Generate social media usernames

Generate social media usernames. The same logic as the free web tool at https://postboost.co/tools/social-media-username-generator. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
free_tool_generate_usernames_request = PostBoost::FreeToolGenerateUsernamesRequest.new({name: 'name_example'}) # FreeToolGenerateUsernamesRequest | 

begin
  # Generate social media usernames
  result = api_instance.generate_usernames(free_tool_generate_usernames_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->generate_usernames: #{e}"
end
```

#### Using the generate_usernames_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolGenerateUsernamesResponse>, Integer, Hash)> generate_usernames_with_http_info(free_tool_generate_usernames_request)

```ruby
begin
  # Generate social media usernames
  data, status_code, headers = api_instance.generate_usernames_with_http_info(free_tool_generate_usernames_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolGenerateUsernamesResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->generate_usernames_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_generate_usernames_request** | [**FreeToolGenerateUsernamesRequest**](FreeToolGenerateUsernamesRequest.md) |  |  |

### Return type

[**FreeToolGenerateUsernamesResponse**](FreeToolGenerateUsernamesResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## generate_youtube_description

> <FreeToolGenerateYoutubeDescriptionResponse> generate_youtube_description(free_tool_generate_youtube_description_request)

Write three YouTube video descriptions with AI (needs a token, spends AI credits)

Write three YouTube video descriptions with AI (needs a token, spends AI credits). The same logic as the free web tool at https://postboost.co/tools/youtube-description-generator. Needs an API token (a scoped key needs the `ai` ability and pays with its own workspace). A new generation spends 1 AI credit of the workspace you name (or your active workspace); a repeated identical request is answered from the cache for free.

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
free_tool_generate_youtube_description_request = PostBoost::FreeToolGenerateYoutubeDescriptionRequest.new({text: 'text_example'}) # FreeToolGenerateYoutubeDescriptionRequest | 

begin
  # Write three YouTube video descriptions with AI (needs a token, spends AI credits)
  result = api_instance.generate_youtube_description(free_tool_generate_youtube_description_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->generate_youtube_description: #{e}"
end
```

#### Using the generate_youtube_description_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolGenerateYoutubeDescriptionResponse>, Integer, Hash)> generate_youtube_description_with_http_info(free_tool_generate_youtube_description_request)

```ruby
begin
  # Write three YouTube video descriptions with AI (needs a token, spends AI credits)
  data, status_code, headers = api_instance.generate_youtube_description_with_http_info(free_tool_generate_youtube_description_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolGenerateYoutubeDescriptionResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->generate_youtube_description_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_generate_youtube_description_request** | [**FreeToolGenerateYoutubeDescriptionRequest**](FreeToolGenerateYoutubeDescriptionRequest.md) |  |  |

### Return type

[**FreeToolGenerateYoutubeDescriptionResponse**](FreeToolGenerateYoutubeDescriptionResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## generate_youtube_titles

> <FreeToolGenerateYoutubeTitlesResponse> generate_youtube_titles(free_tool_generate_youtube_titles_request)

Write five YouTube video titles with AI (needs a token, spends AI credits)

Write five YouTube video titles with AI (needs a token, spends AI credits). The same logic as the free web tool at https://postboost.co/tools/youtube-title-generator. Needs an API token (a scoped key needs the `ai` ability and pays with its own workspace). A new generation spends 1 AI credit of the workspace you name (or your active workspace); a repeated identical request is answered from the cache for free.

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
free_tool_generate_youtube_titles_request = PostBoost::FreeToolGenerateYoutubeTitlesRequest.new({text: 'text_example'}) # FreeToolGenerateYoutubeTitlesRequest | 

begin
  # Write five YouTube video titles with AI (needs a token, spends AI credits)
  result = api_instance.generate_youtube_titles(free_tool_generate_youtube_titles_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->generate_youtube_titles: #{e}"
end
```

#### Using the generate_youtube_titles_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolGenerateYoutubeTitlesResponse>, Integer, Hash)> generate_youtube_titles_with_http_info(free_tool_generate_youtube_titles_request)

```ruby
begin
  # Write five YouTube video titles with AI (needs a token, spends AI credits)
  data, status_code, headers = api_instance.generate_youtube_titles_with_http_info(free_tool_generate_youtube_titles_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolGenerateYoutubeTitlesResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->generate_youtube_titles_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_generate_youtube_titles_request** | [**FreeToolGenerateYoutubeTitlesRequest**](FreeToolGenerateYoutubeTitlesRequest.md) |  |  |

### Return type

[**FreeToolGenerateYoutubeTitlesResponse**](FreeToolGenerateYoutubeTitlesResponse.md)

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


## get_glossary

> <FreeToolGetGlossaryResponse> get_glossary(opts)

Look up social media terms: plain-language definitions by category, with sources and related terms

Look up social media terms: plain-language definitions by category, with sources and related terms. The same logic as the free web tool at https://postboost.co/tools/social-media-glossary. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
opts = {
  q: 'q_example', # String | 
  category: 'metrics' # String | 
}

begin
  # Look up social media terms: plain-language definitions by category, with sources and related terms
  result = api_instance.get_glossary(opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->get_glossary: #{e}"
end
```

#### Using the get_glossary_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolGetGlossaryResponse>, Integer, Hash)> get_glossary_with_http_info(opts)

```ruby
begin
  # Look up social media terms: plain-language definitions by category, with sources and related terms
  data, status_code, headers = api_instance.get_glossary_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolGetGlossaryResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->get_glossary_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **q** | **String** |  | [optional] |
| **category** | **String** |  | [optional] |

### Return type

[**FreeToolGetGlossaryResponse**](FreeToolGetGlossaryResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_hook_templates

> <FreeToolGetHookTemplatesResponse> get_hook_templates(opts)

Get free hook templates for social media posts, filtered by style and network

Get free hook templates for social media posts, filtered by style and network. The same logic as the free web tool at https://postboost.co/tools/hook-generator. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
opts = {
  topic: 'topic_example', # String | 
  category: 'question', # String | 
  network: 'instagram', # String | 
  search: 'search_example' # String | 
}

begin
  # Get free hook templates for social media posts, filtered by style and network
  result = api_instance.get_hook_templates(opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->get_hook_templates: #{e}"
end
```

#### Using the get_hook_templates_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolGetHookTemplatesResponse>, Integer, Hash)> get_hook_templates_with_http_info(opts)

```ruby
begin
  # Get free hook templates for social media posts, filtered by style and network
  data, status_code, headers = api_instance.get_hook_templates_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolGetHookTemplatesResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->get_hook_templates_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **topic** | **String** |  | [optional] |
| **category** | **String** |  | [optional] |
| **network** | **String** |  | [optional] |
| **search** | **String** |  | [optional] |

### Return type

[**FreeToolGetHookTemplatesResponse**](FreeToolGetHookTemplatesResponse.md)

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


## get_safe_zones

> <FreeToolGetSafeZonesResponse> get_safe_zones(free_tool_get_safe_zones_request)

Get the TikTok, Instagram Reels or YouTube Shorts safe zones for a vertical frame

Get the TikTok, Instagram Reels or YouTube Shorts safe zones for a vertical frame. The same logic as the free web tool at https://postboost.co/tools/safe-zone-checker. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
free_tool_get_safe_zones_request = PostBoost::FreeToolGetSafeZonesRequest.new({platform: 'tiktok'}) # FreeToolGetSafeZonesRequest | 

begin
  # Get the TikTok, Instagram Reels or YouTube Shorts safe zones for a vertical frame
  result = api_instance.get_safe_zones(free_tool_get_safe_zones_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->get_safe_zones: #{e}"
end
```

#### Using the get_safe_zones_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolGetSafeZonesResponse>, Integer, Hash)> get_safe_zones_with_http_info(free_tool_get_safe_zones_request)

```ruby
begin
  # Get the TikTok, Instagram Reels or YouTube Shorts safe zones for a vertical frame
  data, status_code, headers = api_instance.get_safe_zones_with_http_info(free_tool_get_safe_zones_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolGetSafeZonesResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->get_safe_zones_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_get_safe_zones_request** | [**FreeToolGetSafeZonesRequest**](FreeToolGetSafeZonesRequest.md) |  |  |

### Return type

[**FreeToolGetSafeZonesResponse**](FreeToolGetSafeZonesResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## get_video_specs

> <FreeToolGetVideoSpecsResponse> get_video_specs(opts)

Get social media video ratios, resolutions, lengths and file size limits per network, with sources

Get social media video ratios, resolutions, lengths and file size limits per network, with sources. The same logic as the free web tool at https://postboost.co/tools/social-media-video-specs. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
opts = {
  network: 'network_example' # String | 
}

begin
  # Get social media video ratios, resolutions, lengths and file size limits per network, with sources
  result = api_instance.get_video_specs(opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->get_video_specs: #{e}"
end
```

#### Using the get_video_specs_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolGetVideoSpecsResponse>, Integer, Hash)> get_video_specs_with_http_info(opts)

```ruby
begin
  # Get social media video ratios, resolutions, lengths and file size limits per network, with sources
  data, status_code, headers = api_instance.get_video_specs_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolGetVideoSpecsResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->get_video_specs_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **network** | **String** |  | [optional] |

### Return type

[**FreeToolGetVideoSpecsResponse**](FreeToolGetVideoSpecsResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_awareness_days

> <FreeToolListAwarenessDaysResponse> list_awareness_days(opts)

List public holidays, awareness days and social media days by date, country, type and topic, with sources

List public holidays, awareness days and social media days by date, country, type and topic, with sources. The same logic as the free web tool at https://postboost.co/tools/social-media-holiday-calendar. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
opts = {
  from: 'from_example', # String | 
  to: 'to_example', # String | 
  country: 'US', # String | 
  type: 'public-holiday', # String | 
  topic: 'business' # String | 
}

begin
  # List public holidays, awareness days and social media days by date, country, type and topic, with sources
  result = api_instance.list_awareness_days(opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->list_awareness_days: #{e}"
end
```

#### Using the list_awareness_days_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolListAwarenessDaysResponse>, Integer, Hash)> list_awareness_days_with_http_info(opts)

```ruby
begin
  # List public holidays, awareness days and social media days by date, country, type and topic, with sources
  data, status_code, headers = api_instance.list_awareness_days_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolListAwarenessDaysResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->list_awareness_days_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **from** | **String** |  | [optional] |
| **to** | **String** |  | [optional] |
| **country** | **String** |  | [optional] |
| **type** | **String** |  | [optional] |
| **topic** | **String** |  | [optional] |

### Return type

[**FreeToolListAwarenessDaysResponse**](FreeToolListAwarenessDaysResponse.md)

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


## pick_giveaway_winners

> <FreeToolPickGiveawayWinnersResponse> pick_giveaway_winners(free_tool_pick_giveaway_winners_request)

Pick giveaway winners with a draw anyone can verify

Pick giveaway winners with a draw anyone can verify. The same logic as the free web tool at https://postboost.co/tools/giveaway-comment-picker. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
free_tool_pick_giveaway_winners_request = PostBoost::FreeToolPickGiveawayWinnersRequest.new({entrants: [PostBoost::FreeToolPickGiveawayWinnersRequestEntrantsInner.new({username: 'username_example'})]}) # FreeToolPickGiveawayWinnersRequest | 

begin
  # Pick giveaway winners with a draw anyone can verify
  result = api_instance.pick_giveaway_winners(free_tool_pick_giveaway_winners_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->pick_giveaway_winners: #{e}"
end
```

#### Using the pick_giveaway_winners_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolPickGiveawayWinnersResponse>, Integer, Hash)> pick_giveaway_winners_with_http_info(free_tool_pick_giveaway_winners_request)

```ruby
begin
  # Pick giveaway winners with a draw anyone can verify
  data, status_code, headers = api_instance.pick_giveaway_winners_with_http_info(free_tool_pick_giveaway_winners_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolPickGiveawayWinnersResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->pick_giveaway_winners_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_pick_giveaway_winners_request** | [**FreeToolPickGiveawayWinnersRequest**](FreeToolPickGiveawayWinnersRequest.md) |  |  |

### Return type

[**FreeToolPickGiveawayWinnersResponse**](FreeToolPickGiveawayWinnersResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## pick_social_media_tool

> <FreeToolPickSocialMediaToolResponse> pick_social_media_tool(free_tool_pick_social_media_tool_request)

Match your needs against social media management tools and see what each one misses

Match your needs against social media management tools and see what each one misses. The same logic as the free web tool at https://postboost.co/tools/social-media-tool-picker. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
free_tool_pick_social_media_tool_request = PostBoost::FreeToolPickSocialMediaToolRequest.new # FreeToolPickSocialMediaToolRequest | 

begin
  # Match your needs against social media management tools and see what each one misses
  result = api_instance.pick_social_media_tool(free_tool_pick_social_media_tool_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->pick_social_media_tool: #{e}"
end
```

#### Using the pick_social_media_tool_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolPickSocialMediaToolResponse>, Integer, Hash)> pick_social_media_tool_with_http_info(free_tool_pick_social_media_tool_request)

```ruby
begin
  # Match your needs against social media management tools and see what each one misses
  data, status_code, headers = api_instance.pick_social_media_tool_with_http_info(free_tool_pick_social_media_tool_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolPickSocialMediaToolResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->pick_social_media_tool_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_pick_social_media_tool_request** | [**FreeToolPickSocialMediaToolRequest**](FreeToolPickSocialMediaToolRequest.md) |  |  |

### Return type

[**FreeToolPickSocialMediaToolResponse**](FreeToolPickSocialMediaToolResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## plan_content_calendar

> <FreeToolPlanContentCalendarResponse> plan_content_calendar(free_tool_plan_content_calendar_request)

Plan a social media content calendar and get it as CSV and ICS

Plan a social media content calendar and get it as CSV and ICS. The same logic as the free web tool at https://postboost.co/tools/social-media-content-calendar-generator. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
free_tool_plan_content_calendar_request = PostBoost::FreeToolPlanContentCalendarRequest.new({start_date: 'start_date_example', posts_per_week: PostBoost::FreeToolPlanContentCalendarRequestPostsPerWeek.new}) # FreeToolPlanContentCalendarRequest | 

begin
  # Plan a social media content calendar and get it as CSV and ICS
  result = api_instance.plan_content_calendar(free_tool_plan_content_calendar_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->plan_content_calendar: #{e}"
end
```

#### Using the plan_content_calendar_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolPlanContentCalendarResponse>, Integer, Hash)> plan_content_calendar_with_http_info(free_tool_plan_content_calendar_request)

```ruby
begin
  # Plan a social media content calendar and get it as CSV and ICS
  data, status_code, headers = api_instance.plan_content_calendar_with_http_info(free_tool_plan_content_calendar_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolPlanContentCalendarResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->plan_content_calendar_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_plan_content_calendar_request** | [**FreeToolPlanContentCalendarRequest**](FreeToolPlanContentCalendarRequest.md) |  |  |

### Return type

[**FreeToolPlanContentCalendarResponse**](FreeToolPlanContentCalendarResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## plan_posting_frequency

> <FreeToolPlanPostingFrequencyResponse> plan_posting_frequency(free_tool_plan_posting_frequency_request)

Plan how often to post on each network

Plan how often to post on each network. The same logic as the free web tool at https://postboost.co/tools/posting-frequency-planner. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
free_tool_plan_posting_frequency_request = PostBoost::FreeToolPlanPostingFrequencyRequest.new({networks: ['instagram'], posts_per_week_capacity: 37}) # FreeToolPlanPostingFrequencyRequest | 

begin
  # Plan how often to post on each network
  result = api_instance.plan_posting_frequency(free_tool_plan_posting_frequency_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->plan_posting_frequency: #{e}"
end
```

#### Using the plan_posting_frequency_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolPlanPostingFrequencyResponse>, Integer, Hash)> plan_posting_frequency_with_http_info(free_tool_plan_posting_frequency_request)

```ruby
begin
  # Plan how often to post on each network
  data, status_code, headers = api_instance.plan_posting_frequency_with_http_info(free_tool_plan_posting_frequency_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolPlanPostingFrequencyResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->plan_posting_frequency_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_plan_posting_frequency_request** | [**FreeToolPlanPostingFrequencyRequest**](FreeToolPlanPostingFrequencyRequest.md) |  |  |

### Return type

[**FreeToolPlanPostingFrequencyResponse**](FreeToolPlanPostingFrequencyResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
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


## score_social_audit

> <FreeToolScoreSocialAuditResponse> score_social_audit(free_tool_score_social_audit_request)

Score a social media audit checklist and get the top fixes

Score a social media audit checklist and get the top fixes. The same logic as the free web tool at https://postboost.co/tools/social-media-audit-template. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
free_tool_score_social_audit_request = PostBoost::FreeToolScoreSocialAuditRequest.new # FreeToolScoreSocialAuditRequest | 

begin
  # Score a social media audit checklist and get the top fixes
  result = api_instance.score_social_audit(free_tool_score_social_audit_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->score_social_audit: #{e}"
end
```

#### Using the score_social_audit_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolScoreSocialAuditResponse>, Integer, Hash)> score_social_audit_with_http_info(free_tool_score_social_audit_request)

```ruby
begin
  # Score a social media audit checklist and get the top fixes
  data, status_code, headers = api_instance.score_social_audit_with_http_info(free_tool_score_social_audit_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolScoreSocialAuditResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->score_social_audit_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_score_social_audit_request** | [**FreeToolScoreSocialAuditRequest**](FreeToolScoreSocialAuditRequest.md) |  |  |

### Return type

[**FreeToolScoreSocialAuditResponse**](FreeToolScoreSocialAuditResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## search_emoji

> <FreeToolSearchEmojiResponse> search_emoji(free_tool_search_emoji_request)

Search emoji by name or keyword, to copy and paste into a post

Search emoji by name or keyword, to copy and paste into a post. The same logic as the free web tool at https://postboost.co/tools/social-media-emoji-picker. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
free_tool_search_emoji_request = PostBoost::FreeToolSearchEmojiRequest.new # FreeToolSearchEmojiRequest | 

begin
  # Search emoji by name or keyword, to copy and paste into a post
  result = api_instance.search_emoji(free_tool_search_emoji_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->search_emoji: #{e}"
end
```

#### Using the search_emoji_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolSearchEmojiResponse>, Integer, Hash)> search_emoji_with_http_info(free_tool_search_emoji_request)

```ruby
begin
  # Search emoji by name or keyword, to copy and paste into a post
  data, status_code, headers = api_instance.search_emoji_with_http_info(free_tool_search_emoji_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolSearchEmojiResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->search_emoji_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_search_emoji_request** | [**FreeToolSearchEmojiRequest**](FreeToolSearchEmojiRequest.md) |  |  |

### Return type

[**FreeToolSearchEmojiResponse**](FreeToolSearchEmojiResponse.md)

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


## summarize_report

> <FreeToolSummarizeReportResponse> summarize_report(free_tool_summarize_report_request)

Summarize social media post metrics into a report

Summarize social media post metrics into a report. The same logic as the free web tool at https://postboost.co/tools/social-media-report-generator. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
free_tool_summarize_report_request = PostBoost::FreeToolSummarizeReportRequest.new({rows: [PostBoost::FreeToolSummarizeReportRequestRowsInner.new]}) # FreeToolSummarizeReportRequest | 

begin
  # Summarize social media post metrics into a report
  result = api_instance.summarize_report(free_tool_summarize_report_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->summarize_report: #{e}"
end
```

#### Using the summarize_report_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolSummarizeReportResponse>, Integer, Hash)> summarize_report_with_http_info(free_tool_summarize_report_request)

```ruby
begin
  # Summarize social media post metrics into a report
  data, status_code, headers = api_instance.summarize_report_with_http_info(free_tool_summarize_report_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolSummarizeReportResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->summarize_report_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_summarize_report_request** | [**FreeToolSummarizeReportRequest**](FreeToolSummarizeReportRequest.md) |  |  |

### Return type

[**FreeToolSummarizeReportResponse**](FreeToolSummarizeReportResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## verify_webhook_signature

> <FreeToolVerifyWebhookSignatureResponse> verify_webhook_signature(free_tool_verify_webhook_signature_request)

Verify an HMAC webhook signature

Verify an HMAC webhook signature. The same logic as the free web tool at https://postboost.co/tools/webhook-signature-verifier. No account needed: call it without a token, or with any API token.

### Examples

```ruby
require 'time'
require 'postboost'

api_instance = PostBoost::FreeToolsApi.new
free_tool_verify_webhook_signature_request = PostBoost::FreeToolVerifyWebhookSignatureRequest.new({body: 'body_example', secret: 'secret_example', signature: 'signature_example'}) # FreeToolVerifyWebhookSignatureRequest | 

begin
  # Verify an HMAC webhook signature
  result = api_instance.verify_webhook_signature(free_tool_verify_webhook_signature_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->verify_webhook_signature: #{e}"
end
```

#### Using the verify_webhook_signature_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FreeToolVerifyWebhookSignatureResponse>, Integer, Hash)> verify_webhook_signature_with_http_info(free_tool_verify_webhook_signature_request)

```ruby
begin
  # Verify an HMAC webhook signature
  data, status_code, headers = api_instance.verify_webhook_signature_with_http_info(free_tool_verify_webhook_signature_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FreeToolVerifyWebhookSignatureResponse>
rescue PostBoost::ApiError => e
  puts "Error when calling FreeToolsApi->verify_webhook_signature_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **free_tool_verify_webhook_signature_request** | [**FreeToolVerifyWebhookSignatureRequest**](FreeToolVerifyWebhookSignatureRequest.md) |  |  |

### Return type

[**FreeToolVerifyWebhookSignatureResponse**](FreeToolVerifyWebhookSignatureResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

