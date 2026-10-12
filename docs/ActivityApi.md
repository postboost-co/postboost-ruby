# PostBoost::ActivityApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**list_api_activity**](ActivityApi.md#list_api_activity) | **GET** /{workspaceUuid}/activity | List API activity |


## list_api_activity

> <ListApiActivity200Response> list_api_activity(workspace_uuid, opts)

List API activity

Every write request (`POST`, `PUT`, `DELETE`) made through the API in this workspace, newest first, with the client that made it and its outcome. Kept for 90 days. Send an `X-PostBoost-Client` header (for example `my-agent/1.2`) to label your requests; otherwise the `User-Agent` is recorded. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::ActivityApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
opts = {
  outcome: PostBoost::ApiActivityOutcome::CREATED, # ApiActivityOutcome | 
  client: 'client_example', # String | Client label prefix, for example `mcp`.
  since: Time.parse('2013-10-20T19:20:30+01:00'), # Time | Only entries at or after this time (UTC).
  page: 56 # Integer | 
}

begin
  # List API activity
  result = api_instance.list_api_activity(workspace_uuid, opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling ActivityApi->list_api_activity: #{e}"
end
```

#### Using the list_api_activity_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListApiActivity200Response>, Integer, Hash)> list_api_activity_with_http_info(workspace_uuid, opts)

```ruby
begin
  # List API activity
  data, status_code, headers = api_instance.list_api_activity_with_http_info(workspace_uuid, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListApiActivity200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling ActivityApi->list_api_activity_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **outcome** | [**ApiActivityOutcome**](.md) |  | [optional] |
| **client** | **String** | Client label prefix, for example &#x60;mcp&#x60;. | [optional] |
| **since** | **Time** | Only entries at or after this time (UTC). | [optional] |
| **page** | **Integer** |  | [optional][default to 1] |

### Return type

[**ListApiActivity200Response**](ListApiActivity200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

