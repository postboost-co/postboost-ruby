# PostBoost::AnalyticsApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_report_export**](AnalyticsApi.md#create_report_export) | **POST** /{workspaceUuid}/reports/exports | Create a report export |
| [**download_report_export**](AnalyticsApi.md#download_report_export) | **GET** /{workspaceUuid}/reports/exports/{exportUuid}/download | Download a report file |
| [**get_account_analytics**](AnalyticsApi.md#get_account_analytics) | **GET** /{workspaceUuid}/analytics/accounts/{accountUuid} | Get account analytics |
| [**get_analytics_summary**](AnalyticsApi.md#get_analytics_summary) | **GET** /{workspaceUuid}/analytics | Get analytics summary |
| [**get_best_posting_times**](AnalyticsApi.md#get_best_posting_times) | **GET** /{workspaceUuid}/analytics/best-times | Get best posting times |
| [**get_post_analytics_0**](AnalyticsApi.md#get_post_analytics_0) | **GET** /{workspaceUuid}/posts/{postUuid}/analytics | Get post analytics |
| [**get_posting_times**](AnalyticsApi.md#get_posting_times) | **GET** /{workspaceUuid}/analytics/posting-times | Get posting times heatmap |
| [**get_report_branding**](AnalyticsApi.md#get_report_branding) | **GET** /{workspaceUuid}/report-branding | Get the report branding |
| [**get_report_export**](AnalyticsApi.md#get_report_export) | **GET** /{workspaceUuid}/reports/exports/{exportUuid} | Get a report export |
| [**list_report_exports**](AnalyticsApi.md#list_report_exports) | **GET** /{workspaceUuid}/reports/exports | List report exports |
| [**update_report_branding**](AnalyticsApi.md#update_report_branding) | **PUT** /{workspaceUuid}/report-branding | Update the report branding |
| [**upload_report_branding_logo**](AnalyticsApi.md#upload_report_branding_logo) | **POST** /{workspaceUuid}/report-branding/logo | Upload the report logo |


## create_report_export

> <CreateReportExport201Response> create_report_export(workspace_uuid, report_export_input)

Create a report export

Generates a report for a period (default `last_month`) or a custom `date_from`/`date_to` range: a branded PDF (summary, accounts, top 10 posts; the header uses the report branding) or a CSV with one row per published post and account (`dataset: posts`, default) or per account (`dataset: accounts`). CSV files are UTF-8 with a byte order mark. At most 500 posts per report. The file is ready when the call returns; fetch it from `download_url` with the same token. Admins and members only; 20 per minute. 

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
report_export_input = PostBoost::ReportExportInput.new({format: 'csv'}) # ReportExportInput | 

begin
  # Create a report export
  result = api_instance.create_report_export(workspace_uuid, report_export_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AnalyticsApi->create_report_export: #{e}"
end
```

#### Using the create_report_export_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateReportExport201Response>, Integer, Hash)> create_report_export_with_http_info(workspace_uuid, report_export_input)

```ruby
begin
  # Create a report export
  data, status_code, headers = api_instance.create_report_export_with_http_info(workspace_uuid, report_export_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateReportExport201Response>
rescue PostBoost::ApiError => e
  puts "Error when calling AnalyticsApi->create_report_export_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **report_export_input** | [**ReportExportInput**](ReportExportInput.md) |  |  |

### Return type

[**CreateReportExport201Response**](CreateReportExport201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## download_report_export

> File download_report_export(workspace_uuid, export_uuid)

Download a report file

The PDF or CSV file. `410` once it expired (7 days) or if the export failed.

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
export_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the report export.

begin
  # Download a report file
  result = api_instance.download_report_export(workspace_uuid, export_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AnalyticsApi->download_report_export: #{e}"
end
```

#### Using the download_report_export_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(File, Integer, Hash)> download_report_export_with_http_info(workspace_uuid, export_uuid)

```ruby
begin
  # Download a report file
  data, status_code, headers = api_instance.download_report_export_with_http_info(workspace_uuid, export_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => File
rescue PostBoost::ApiError => e
  puts "Error when calling AnalyticsApi->download_report_export_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **export_uuid** | **String** | UUID of the report export. |  |

### Return type

**File**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/pdf, text/csv, application/json


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


## get_report_branding

> <GetReportBranding200Response> get_report_branding(workspace_uuid)

Get the report branding

The white-label header of the workspace's PDF reports. Unset fields are `null`; the workspace name is used then.

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

begin
  # Get the report branding
  result = api_instance.get_report_branding(workspace_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AnalyticsApi->get_report_branding: #{e}"
end
```

#### Using the get_report_branding_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetReportBranding200Response>, Integer, Hash)> get_report_branding_with_http_info(workspace_uuid)

```ruby
begin
  # Get the report branding
  data, status_code, headers = api_instance.get_report_branding_with_http_info(workspace_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetReportBranding200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling AnalyticsApi->get_report_branding_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |

### Return type

[**GetReportBranding200Response**](GetReportBranding200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_report_export

> <CreateReportExport201Response> get_report_export(workspace_uuid, export_uuid)

Get a report export

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
export_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the report export.

begin
  # Get a report export
  result = api_instance.get_report_export(workspace_uuid, export_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AnalyticsApi->get_report_export: #{e}"
end
```

#### Using the get_report_export_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateReportExport201Response>, Integer, Hash)> get_report_export_with_http_info(workspace_uuid, export_uuid)

```ruby
begin
  # Get a report export
  data, status_code, headers = api_instance.get_report_export_with_http_info(workspace_uuid, export_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateReportExport201Response>
rescue PostBoost::ApiError => e
  puts "Error when calling AnalyticsApi->get_report_export_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **export_uuid** | **String** | UUID of the report export. |  |

### Return type

[**CreateReportExport201Response**](CreateReportExport201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_report_exports

> <ListReportExports200Response> list_report_exports(workspace_uuid)

List report exports

The workspace's latest 50 report exports, newest first. Files can be downloaded for 7 days.

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

begin
  # List report exports
  result = api_instance.list_report_exports(workspace_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AnalyticsApi->list_report_exports: #{e}"
end
```

#### Using the list_report_exports_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListReportExports200Response>, Integer, Hash)> list_report_exports_with_http_info(workspace_uuid)

```ruby
begin
  # List report exports
  data, status_code, headers = api_instance.list_report_exports_with_http_info(workspace_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListReportExports200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling AnalyticsApi->list_report_exports_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |

### Return type

[**ListReportExports200Response**](ListReportExports200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_report_branding

> <GetReportBranding200Response> update_report_branding(workspace_uuid, report_branding_input)

Update the report branding

Name, colour and footer of PDF reports. Fields you leave out keep their value. Upload the logo with `uploadReportBrandingLogo`. Admins and members only.

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
report_branding_input = PostBoost::ReportBrandingInput.new # ReportBrandingInput | 

begin
  # Update the report branding
  result = api_instance.update_report_branding(workspace_uuid, report_branding_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AnalyticsApi->update_report_branding: #{e}"
end
```

#### Using the update_report_branding_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetReportBranding200Response>, Integer, Hash)> update_report_branding_with_http_info(workspace_uuid, report_branding_input)

```ruby
begin
  # Update the report branding
  data, status_code, headers = api_instance.update_report_branding_with_http_info(workspace_uuid, report_branding_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetReportBranding200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling AnalyticsApi->update_report_branding_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **report_branding_input** | [**ReportBrandingInput**](ReportBrandingInput.md) |  |  |

### Return type

[**GetReportBranding200Response**](GetReportBranding200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## upload_report_branding_logo

> <GetReportBranding200Response> upload_report_branding_logo(workspace_uuid, logo)

Upload the report logo

PNG or JPEG, up to 1 MB (SVG is not accepted). Replaces the current logo. Admins and members only.

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
logo = File.new('/path/to/some/file') # File | 

begin
  # Upload the report logo
  result = api_instance.upload_report_branding_logo(workspace_uuid, logo)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AnalyticsApi->upload_report_branding_logo: #{e}"
end
```

#### Using the upload_report_branding_logo_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetReportBranding200Response>, Integer, Hash)> upload_report_branding_logo_with_http_info(workspace_uuid, logo)

```ruby
begin
  # Upload the report logo
  data, status_code, headers = api_instance.upload_report_branding_logo_with_http_info(workspace_uuid, logo)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetReportBranding200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling AnalyticsApi->upload_report_branding_logo_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **logo** | **File** |  |  |

### Return type

[**GetReportBranding200Response**](GetReportBranding200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json

