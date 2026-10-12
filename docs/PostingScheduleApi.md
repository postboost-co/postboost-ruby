# PostBoost::PostingScheduleApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_posting_schedule**](PostingScheduleApi.md#get_posting_schedule) | **GET** /{workspaceUuid}/posting-schedule | Get the posting schedule |
| [**get_recommended_posting_times**](PostingScheduleApi.md#get_recommended_posting_times) | **GET** /{workspaceUuid}/posting-schedule/recommended | Get recommended posting times |
| [**list_queue_slots**](PostingScheduleApi.md#list_queue_slots) | **GET** /{workspaceUuid}/queue/slots | List upcoming queue slots |
| [**reset_account_posting_schedule**](PostingScheduleApi.md#reset_account_posting_schedule) | **DELETE** /{workspaceUuid}/posting-schedule/{accountId} | Reset an account schedule |
| [**update_posting_schedule**](PostingScheduleApi.md#update_posting_schedule) | **PUT** /{workspaceUuid}/posting-schedule | Set the posting schedule |


## get_posting_schedule

> <GetPostingSchedule200Response> get_posting_schedule(workspace_uuid, opts)

Get the posting schedule

The queue's posting times: per weekday, a list of clock times in the schedule's timezone. `account_id=0` is the workspace schedule. An account without its own schedule follows the workspace one (`inherited: true`, `source_account_id: 0`). Posts added to the queue take the next free time. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::PostingScheduleApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
opts = {
  account_id: 56 # Integer | `0` (default) for the workspace schedule, or an account `id`.
}

begin
  # Get the posting schedule
  result = api_instance.get_posting_schedule(workspace_uuid, opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling PostingScheduleApi->get_posting_schedule: #{e}"
end
```

#### Using the get_posting_schedule_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetPostingSchedule200Response>, Integer, Hash)> get_posting_schedule_with_http_info(workspace_uuid, opts)

```ruby
begin
  # Get the posting schedule
  data, status_code, headers = api_instance.get_posting_schedule_with_http_info(workspace_uuid, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetPostingSchedule200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling PostingScheduleApi->get_posting_schedule_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **account_id** | **Integer** | &#x60;0&#x60; (default) for the workspace schedule, or an account &#x60;id&#x60;. | [optional][default to 0] |

### Return type

[**GetPostingSchedule200Response**](GetPostingSchedule200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_recommended_posting_times

> <RecommendedPostingTimes> get_recommended_posting_times(workspace_uuid, opts)

Get recommended posting times

Suggested posting times from past engagement, in the schedule's timezone. `has_data` is false until there is enough analytics history. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::PostingScheduleApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
opts = {
  account_id: 56, # Integer | `0` (default) for the workspace schedule, or an account `id`.
  slots_per_day: 56 # Integer | Times to suggest per day (1 to 6).
}

begin
  # Get recommended posting times
  result = api_instance.get_recommended_posting_times(workspace_uuid, opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling PostingScheduleApi->get_recommended_posting_times: #{e}"
end
```

#### Using the get_recommended_posting_times_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<RecommendedPostingTimes>, Integer, Hash)> get_recommended_posting_times_with_http_info(workspace_uuid, opts)

```ruby
begin
  # Get recommended posting times
  data, status_code, headers = api_instance.get_recommended_posting_times_with_http_info(workspace_uuid, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <RecommendedPostingTimes>
rescue PostBoost::ApiError => e
  puts "Error when calling PostingScheduleApi->get_recommended_posting_times_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **account_id** | **Integer** | &#x60;0&#x60; (default) for the workspace schedule, or an account &#x60;id&#x60;. | [optional][default to 0] |
| **slots_per_day** | **Integer** | Times to suggest per day (1 to 6). | [optional] |

### Return type

[**RecommendedPostingTimes**](RecommendedPostingTimes.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_queue_slots

> <QueueSlots> list_queue_slots(workspace_uuid, opts)

List upcoming queue slots

The queue read forward: upcoming posting times, filled by scheduled posts where they land on one. Page with `after` set to the previous `next_cursor`. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::PostingScheduleApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
opts = {
  account_id: 56, # Integer | `0` (default) for the workspace schedule, or an account `id`.
  after: 'after_example' # String | Start after this time (`Y-m-d H:i:s`, UTC), from `next_cursor`.
}

begin
  # List upcoming queue slots
  result = api_instance.list_queue_slots(workspace_uuid, opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling PostingScheduleApi->list_queue_slots: #{e}"
end
```

#### Using the list_queue_slots_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<QueueSlots>, Integer, Hash)> list_queue_slots_with_http_info(workspace_uuid, opts)

```ruby
begin
  # List upcoming queue slots
  data, status_code, headers = api_instance.list_queue_slots_with_http_info(workspace_uuid, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <QueueSlots>
rescue PostBoost::ApiError => e
  puts "Error when calling PostingScheduleApi->list_queue_slots_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **account_id** | **Integer** | &#x60;0&#x60; (default) for the workspace schedule, or an account &#x60;id&#x60;. | [optional][default to 0] |
| **after** | **String** | Start after this time (&#x60;Y-m-d H:i:s&#x60;, UTC), from &#x60;next_cursor&#x60;. | [optional] |

### Return type

[**QueueSlots**](QueueSlots.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## reset_account_posting_schedule

> <GetPostingSchedule200Response> reset_account_posting_schedule(workspace_uuid, account_id)

Reset an account schedule

Removes the account's own schedule so it follows the workspace schedule again. Workspace admins only. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::PostingScheduleApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
account_id = 56 # Integer | The account `id`.

begin
  # Reset an account schedule
  result = api_instance.reset_account_posting_schedule(workspace_uuid, account_id)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling PostingScheduleApi->reset_account_posting_schedule: #{e}"
end
```

#### Using the reset_account_posting_schedule_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetPostingSchedule200Response>, Integer, Hash)> reset_account_posting_schedule_with_http_info(workspace_uuid, account_id)

```ruby
begin
  # Reset an account schedule
  data, status_code, headers = api_instance.reset_account_posting_schedule_with_http_info(workspace_uuid, account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetPostingSchedule200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling PostingScheduleApi->reset_account_posting_schedule_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **account_id** | **Integer** | The account &#x60;id&#x60;. |  |

### Return type

[**GetPostingSchedule200Response**](GetPostingSchedule200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_posting_schedule

> <GetPostingSchedule200Response> update_posting_schedule(workspace_uuid, posting_schedule_input)

Set the posting schedule

Sets the workspace schedule (`account_id: 0`) or gives one account its own schedule. Send all seven weekdays (ids 1 to 6 for Monday to Saturday, 0 for Sunday). Workspace admins only. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::PostingScheduleApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
posting_schedule_input = PostBoost::PostingScheduleInput.new({account_id: 37, timezone: 'Europe/Amsterdam', times: [PostBoost::PostingScheduleDay.new({id: 37, status: false, times: [PostBoost::PostingScheduleDayTimesInner.new({value: '09:00'})]})]}) # PostingScheduleInput | 

begin
  # Set the posting schedule
  result = api_instance.update_posting_schedule(workspace_uuid, posting_schedule_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling PostingScheduleApi->update_posting_schedule: #{e}"
end
```

#### Using the update_posting_schedule_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetPostingSchedule200Response>, Integer, Hash)> update_posting_schedule_with_http_info(workspace_uuid, posting_schedule_input)

```ruby
begin
  # Set the posting schedule
  data, status_code, headers = api_instance.update_posting_schedule_with_http_info(workspace_uuid, posting_schedule_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetPostingSchedule200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling PostingScheduleApi->update_posting_schedule_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **posting_schedule_input** | [**PostingScheduleInput**](PostingScheduleInput.md) |  |  |

### Return type

[**GetPostingSchedule200Response**](GetPostingSchedule200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

