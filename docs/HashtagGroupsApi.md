# PostBoost::HashtagGroupsApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_hashtag_group**](HashtagGroupsApi.md#create_hashtag_group) | **POST** /{workspaceUuid}/hashtag-groups | Create a hashtag group |
| [**delete_hashtag_group**](HashtagGroupsApi.md#delete_hashtag_group) | **DELETE** /{workspaceUuid}/hashtag-groups/{hashtagGroupId} | Delete a hashtag group |
| [**get_hashtag_group**](HashtagGroupsApi.md#get_hashtag_group) | **GET** /{workspaceUuid}/hashtag-groups/{hashtagGroupId} | Get a hashtag group |
| [**list_hashtag_groups**](HashtagGroupsApi.md#list_hashtag_groups) | **GET** /{workspaceUuid}/hashtag-groups | List hashtag groups |
| [**update_hashtag_group**](HashtagGroupsApi.md#update_hashtag_group) | **PUT** /{workspaceUuid}/hashtag-groups/{hashtagGroupId} | Update a hashtag group |


## create_hashtag_group

> <CreateHashtagGroup201Response> create_hashtag_group(workspace_uuid, hashtag_group_input)

Create a hashtag group

Saves a named set of hashtags (up to 3000 characters). Admins and members only (not viewers). 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::HashtagGroupsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
hashtag_group_input = PostBoost::HashtagGroupInput.new({name: 'name_example', content: 'content_example'}) # HashtagGroupInput | 

begin
  # Create a hashtag group
  result = api_instance.create_hashtag_group(workspace_uuid, hashtag_group_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling HashtagGroupsApi->create_hashtag_group: #{e}"
end
```

#### Using the create_hashtag_group_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateHashtagGroup201Response>, Integer, Hash)> create_hashtag_group_with_http_info(workspace_uuid, hashtag_group_input)

```ruby
begin
  # Create a hashtag group
  data, status_code, headers = api_instance.create_hashtag_group_with_http_info(workspace_uuid, hashtag_group_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateHashtagGroup201Response>
rescue PostBoost::ApiError => e
  puts "Error when calling HashtagGroupsApi->create_hashtag_group_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **hashtag_group_input** | [**HashtagGroupInput**](HashtagGroupInput.md) |  |  |

### Return type

[**CreateHashtagGroup201Response**](CreateHashtagGroup201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_hashtag_group

> delete_hashtag_group(workspace_uuid, hashtag_group_id)

Delete a hashtag group

Admins and members only (not viewers). 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::HashtagGroupsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
hashtag_group_id = 'hashtag_group_id_example' # String | The hashtag group `id`.

begin
  # Delete a hashtag group
  api_instance.delete_hashtag_group(workspace_uuid, hashtag_group_id)
rescue PostBoost::ApiError => e
  puts "Error when calling HashtagGroupsApi->delete_hashtag_group: #{e}"
end
```

#### Using the delete_hashtag_group_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_hashtag_group_with_http_info(workspace_uuid, hashtag_group_id)

```ruby
begin
  # Delete a hashtag group
  data, status_code, headers = api_instance.delete_hashtag_group_with_http_info(workspace_uuid, hashtag_group_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue PostBoost::ApiError => e
  puts "Error when calling HashtagGroupsApi->delete_hashtag_group_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **hashtag_group_id** | **String** | The hashtag group &#x60;id&#x60;. |  |

### Return type

nil (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_hashtag_group

> <CreateHashtagGroup201Response> get_hashtag_group(workspace_uuid, hashtag_group_id)

Get a hashtag group

One hashtag group. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::HashtagGroupsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
hashtag_group_id = 'hashtag_group_id_example' # String | The hashtag group `id`.

begin
  # Get a hashtag group
  result = api_instance.get_hashtag_group(workspace_uuid, hashtag_group_id)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling HashtagGroupsApi->get_hashtag_group: #{e}"
end
```

#### Using the get_hashtag_group_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateHashtagGroup201Response>, Integer, Hash)> get_hashtag_group_with_http_info(workspace_uuid, hashtag_group_id)

```ruby
begin
  # Get a hashtag group
  data, status_code, headers = api_instance.get_hashtag_group_with_http_info(workspace_uuid, hashtag_group_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateHashtagGroup201Response>
rescue PostBoost::ApiError => e
  puts "Error when calling HashtagGroupsApi->get_hashtag_group_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **hashtag_group_id** | **String** | The hashtag group &#x60;id&#x60;. |  |

### Return type

[**CreateHashtagGroup201Response**](CreateHashtagGroup201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_hashtag_groups

> <ListHashtagGroups200Response> list_hashtag_groups(workspace_uuid, opts)

List hashtag groups

Saved hashtag sets of the workspace, newest first. Paginated with `page` and `per_page` (default 100). 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::HashtagGroupsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
opts = {
  page: 56, # Integer | Page number (1-based).
  per_page: 56 # Integer | Items per page, 1-100.
}

begin
  # List hashtag groups
  result = api_instance.list_hashtag_groups(workspace_uuid, opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling HashtagGroupsApi->list_hashtag_groups: #{e}"
end
```

#### Using the list_hashtag_groups_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListHashtagGroups200Response>, Integer, Hash)> list_hashtag_groups_with_http_info(workspace_uuid, opts)

```ruby
begin
  # List hashtag groups
  data, status_code, headers = api_instance.list_hashtag_groups_with_http_info(workspace_uuid, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListHashtagGroups200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling HashtagGroupsApi->list_hashtag_groups_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **page** | **Integer** | Page number (1-based). | [optional][default to 1] |
| **per_page** | **Integer** | Items per page, 1-100. | [optional][default to 100] |

### Return type

[**ListHashtagGroups200Response**](ListHashtagGroups200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_hashtag_group

> <CreateHashtagGroup201Response> update_hashtag_group(workspace_uuid, hashtag_group_id, hashtag_group_input)

Update a hashtag group

Admins and members only (not viewers). 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::HashtagGroupsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
hashtag_group_id = 'hashtag_group_id_example' # String | The hashtag group `id`.
hashtag_group_input = PostBoost::HashtagGroupInput.new({name: 'name_example', content: 'content_example'}) # HashtagGroupInput | 

begin
  # Update a hashtag group
  result = api_instance.update_hashtag_group(workspace_uuid, hashtag_group_id, hashtag_group_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling HashtagGroupsApi->update_hashtag_group: #{e}"
end
```

#### Using the update_hashtag_group_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateHashtagGroup201Response>, Integer, Hash)> update_hashtag_group_with_http_info(workspace_uuid, hashtag_group_id, hashtag_group_input)

```ruby
begin
  # Update a hashtag group
  data, status_code, headers = api_instance.update_hashtag_group_with_http_info(workspace_uuid, hashtag_group_id, hashtag_group_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateHashtagGroup201Response>
rescue PostBoost::ApiError => e
  puts "Error when calling HashtagGroupsApi->update_hashtag_group_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **hashtag_group_id** | **String** | The hashtag group &#x60;id&#x60;. |  |
| **hashtag_group_input** | [**HashtagGroupInput**](HashtagGroupInput.md) |  |  |

### Return type

[**CreateHashtagGroup201Response**](CreateHashtagGroup201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

