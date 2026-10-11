# PostBoost::AnalyticsApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_account_analytics**](AnalyticsApi.md#get_account_analytics) | **GET** /{workspaceUuid}/analytics/accounts/{accountUuid} | Get account analytics |
| [**get_analytics_summary**](AnalyticsApi.md#get_analytics_summary) | **GET** /{workspaceUuid}/analytics | Get analytics summary |
| [**get_best_posting_times**](AnalyticsApi.md#get_best_posting_times) | **GET** /{workspaceUuid}/analytics/best-times | Get best posting times |
| [**get_post_analytics_0**](AnalyticsApi.md#get_post_analytics_0) | **GET** /{workspaceUuid}/posts/{postUuid}/analytics | Get post analytics |
| [**get_posting_times**](AnalyticsApi.md#get_posting_times) | **GET** /{workspaceUuid}/analytics/posting-times | Get posting times heatmap |


## get_account_analytics

> <AccountAnalytics> get_account_analytics(workspace_uuid, account_uuid, opts)

Get account analytics

Analytics for one account. `type` selects one of the tabs the account supports (listed in `tabs` of the response); returns `422` when the account does not support analytics.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::AnalyticsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
account_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the social media account.
opts = {
  period: 'this_week', # String | Preset reporting period. Ignored when `date_from` and `date_to` are given.
  date_from: Date.parse('2013-10-20'), # Date | Start of a custom range (Y-m-d). Required with `date_to`; the range may span at most 366 days.
  date_to: Date.parse('2013-10-20'), # Date | End of a custom range (Y-m-d). Required with `date_from`; must not be before it.
  type: 'type_example', # String | Analytics tab. Defaults to the account's default tab.
  page: 56, # Integer | Page for list-style tabs (for example per-post metrics).
  per_page: 56, # Integer | 
  sort_by: 'sort_by_example', # String | 
  sort_dir: 'asc' # String | 
}

begin
  # Get account analytics
  result = api_instance.get_account_analytics(workspace_uuid, account_uuid, opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AnalyticsApi->get_account_analytics: #{e}"
end
```

#### Using the get_account_analytics_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AccountAnalytics>, Integer, Hash)> get_account_analytics_with_http_info(workspace_uuid, account_uuid, opts)

```ruby
begin
  # Get account analytics
  data, status_code, headers = api_instance.get_account_analytics_with_http_info(workspace_uuid, account_uuid, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AccountAnalytics>
rescue PostBoost::ApiError => e
  puts "Error when calling AnalyticsApi->get_account_analytics_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **account_uuid** | **String** | UUID of the social media account. |  |
| **period** | **String** | Preset reporting period. Ignored when &#x60;date_from&#x60; and &#x60;date_to&#x60; are given. | [optional][default to &#39;this_month&#39;] |
| **date_from** | **Date** | Start of a custom range (Y-m-d). Required with &#x60;date_to&#x60;; the range may span at most 366 days. | [optional] |
| **date_to** | **Date** | End of a custom range (Y-m-d). Required with &#x60;date_from&#x60;; must not be before it. | [optional] |
| **type** | **String** | Analytics tab. Defaults to the account&#39;s default tab. | [optional] |
| **page** | **Integer** | Page for list-style tabs (for example per-post metrics). | [optional][default to 1] |
| **per_page** | **Integer** |  | [optional] |
| **sort_by** | **String** |  | [optional] |
| **sort_dir** | **String** |  | [optional][default to &#39;desc&#39;] |

### Return type

[**AccountAnalytics**](AccountAnalytics.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_analytics_summary

> <AnalyticsSummary> get_analytics_summary(workspace_uuid, opts)

Get analytics summary

Cross-platform summary (followers, growth, posts, leaderboard, posting streak) over every account that supports analytics, for a preset period or a custom date range.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::AnalyticsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
opts = {
  period: 'this_week', # String | Preset reporting period. Ignored when `date_from` and `date_to` are given.
  date_from: Date.parse('2013-10-20'), # Date | Start of a custom range (Y-m-d). Required with `date_to`; the range may span at most 366 days.
  date_to: Date.parse('2013-10-20') # Date | End of a custom range (Y-m-d). Required with `date_from`; must not be before it.
}

begin
  # Get analytics summary
  result = api_instance.get_analytics_summary(workspace_uuid, opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AnalyticsApi->get_analytics_summary: #{e}"
end
```

#### Using the get_analytics_summary_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AnalyticsSummary>, Integer, Hash)> get_analytics_summary_with_http_info(workspace_uuid, opts)

```ruby
begin
  # Get analytics summary
  data, status_code, headers = api_instance.get_analytics_summary_with_http_info(workspace_uuid, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AnalyticsSummary>
rescue PostBoost::ApiError => e
  puts "Error when calling AnalyticsApi->get_analytics_summary_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **period** | **String** | Preset reporting period. Ignored when &#x60;date_from&#x60; and &#x60;date_to&#x60; are given. | [optional][default to &#39;this_month&#39;] |
| **date_from** | **Date** | Start of a custom range (Y-m-d). Required with &#x60;date_to&#x60;; the range may span at most 366 days. | [optional] |
| **date_to** | **Date** | End of a custom range (Y-m-d). Required with &#x60;date_from&#x60;; must not be before it. | [optional] |

### Return type

[**AnalyticsSummary**](AnalyticsSummary.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_best_posting_times

> <BestPostingTimes> get_best_posting_times(workspace_uuid, opts)

Get best posting times

The next recommended date and time per account, on or after `from` (never in the past), within the next 14 days.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::AnalyticsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
opts = {
  accounts: ['inner_example'], # Array<String> | Account UUIDs. Defaults to every account in the workspace.
  from: Date.parse('2013-10-20'), # Date | Earliest date to recommend (Y-m-d). Defaults to now.
  timezone: 'timezone_example' # String | Timezone for `from` and the returned times. Defaults to the workspace timezone.
}

begin
  # Get best posting times
  result = api_instance.get_best_posting_times(workspace_uuid, opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AnalyticsApi->get_best_posting_times: #{e}"
end
```

#### Using the get_best_posting_times_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BestPostingTimes>, Integer, Hash)> get_best_posting_times_with_http_info(workspace_uuid, opts)

```ruby
begin
  # Get best posting times
  data, status_code, headers = api_instance.get_best_posting_times_with_http_info(workspace_uuid, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BestPostingTimes>
rescue PostBoost::ApiError => e
  puts "Error when calling AnalyticsApi->get_best_posting_times_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **accounts** | [**Array&lt;String&gt;**](String.md) | Account UUIDs. Defaults to every account in the workspace. | [optional] |
| **from** | **Date** | Earliest date to recommend (Y-m-d). Defaults to now. | [optional] |
| **timezone** | **String** | Timezone for &#x60;from&#x60; and the returned times. Defaults to the workspace timezone. | [optional] |

### Return type

[**BestPostingTimes**](BestPostingTimes.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_post_analytics_0

> <PostAnalytics> get_post_analytics_0(workspace_uuid, post_uuid)

Get post analytics

Engagement metrics for a published post across its accounts (also works for trashed posts), with totals, trends and the best-performing account.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::AnalyticsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
post_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the post.

begin
  # Get post analytics
  result = api_instance.get_post_analytics_0(workspace_uuid, post_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AnalyticsApi->get_post_analytics_0: #{e}"
end
```

#### Using the get_post_analytics_0_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PostAnalytics>, Integer, Hash)> get_post_analytics_0_with_http_info(workspace_uuid, post_uuid)

```ruby
begin
  # Get post analytics
  data, status_code, headers = api_instance.get_post_analytics_0_with_http_info(workspace_uuid, post_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PostAnalytics>
rescue PostBoost::ApiError => e
  puts "Error when calling AnalyticsApi->get_post_analytics_0_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **post_uuid** | **String** | UUID of the post. |  |

### Return type

[**PostAnalytics**](PostAnalytics.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_posting_times

> <PostingTimes> get_posting_times(workspace_uuid, opts)

Get posting times heatmap

Engagement scores per weekday and hour, merged across the given accounts (all accounts when none is given), in the requested timezone. Also returns up to three recommended slots.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::AnalyticsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
opts = {
  accounts: ['inner_example'], # Array<String> | Account UUIDs. Defaults to every account in the workspace.
  timezone: 'Europe/Istanbul' # String | Timezone the grid is expressed in. Defaults to the workspace timezone.
}

begin
  # Get posting times heatmap
  result = api_instance.get_posting_times(workspace_uuid, opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AnalyticsApi->get_posting_times: #{e}"
end
```

#### Using the get_posting_times_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PostingTimes>, Integer, Hash)> get_posting_times_with_http_info(workspace_uuid, opts)

```ruby
begin
  # Get posting times heatmap
  data, status_code, headers = api_instance.get_posting_times_with_http_info(workspace_uuid, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PostingTimes>
rescue PostBoost::ApiError => e
  puts "Error when calling AnalyticsApi->get_posting_times_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **accounts** | [**Array&lt;String&gt;**](String.md) | Account UUIDs. Defaults to every account in the workspace. | [optional] |
| **timezone** | **String** | Timezone the grid is expressed in. Defaults to the workspace timezone. | [optional] |

### Return type

[**PostingTimes**](PostingTimes.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

