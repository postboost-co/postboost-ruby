# PostBoost::PostsApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**add_post_to_queue**](PostsApi.md#add_post_to_queue) | **POST** /{workspaceUuid}/posts/add-to-queue/{postUuid} | Add post to queue |
| [**approve_post**](PostsApi.md#approve_post) | **POST** /{workspaceUuid}/posts/approve/{postUuid} | Approve post |
| [**create_post**](PostsApi.md#create_post) | **POST** /{workspaceUuid}/posts | Create post |
| [**delete_post**](PostsApi.md#delete_post) | **DELETE** /{workspaceUuid}/posts/{postUuid} | Delete post |
| [**delete_posts_bulk**](PostsApi.md#delete_posts_bulk) | **DELETE** /{workspaceUuid}/posts | Delete posts (bulk) |
| [**get_post**](PostsApi.md#get_post) | **GET** /{workspaceUuid}/posts/{postUuid} | Get post |
| [**list_posts**](PostsApi.md#list_posts) | **GET** /{workspaceUuid}/posts | List posts |
| [**schedule_post**](PostsApi.md#schedule_post) | **POST** /{workspaceUuid}/posts/schedule/{postUuid} | Schedule post |
| [**update_post**](PostsApi.md#update_post) | **PUT** /{workspaceUuid}/posts/{postUuid} | Update post |


## add_post_to_queue

> <ScheduleResult> add_post_to_queue(workspace_uuid, post_uuid)

Add post to queue

Add an existing post to the smart publishing queue.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::PostsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
post_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the post.

begin
  # Add post to queue
  result = api_instance.add_post_to_queue(workspace_uuid, post_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->add_post_to_queue: #{e}"
end
```

#### Using the add_post_to_queue_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ScheduleResult>, Integer, Hash)> add_post_to_queue_with_http_info(workspace_uuid, post_uuid)

```ruby
begin
  # Add post to queue
  data, status_code, headers = api_instance.add_post_to_queue_with_http_info(workspace_uuid, post_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ScheduleResult>
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->add_post_to_queue_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **post_uuid** | **String** | UUID of the post. |  |

### Return type

[**ScheduleResult**](ScheduleResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## approve_post

> <ScheduleResult> approve_post(workspace_uuid, post_uuid)

Approve post

Approve a post that is pending review.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::PostsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
post_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the post.

begin
  # Approve post
  result = api_instance.approve_post(workspace_uuid, post_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->approve_post: #{e}"
end
```

#### Using the approve_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ScheduleResult>, Integer, Hash)> approve_post_with_http_info(workspace_uuid, post_uuid)

```ruby
begin
  # Approve post
  data, status_code, headers = api_instance.approve_post_with_http_info(workspace_uuid, post_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ScheduleResult>
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->approve_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **post_uuid** | **String** | UUID of the post. |  |

### Return type

[**ScheduleResult**](ScheduleResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## create_post

> <Post> create_post(workspace_uuid, post_input)

Create post

Create a new post. Use `schedule: true` with `date` and `time` to schedule, `schedule_now: true` to publish immediately, or `queue: true` to add to the smart publishing queue. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::PostsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
post_input = PostBoost::PostInput.new({versions: [PostBoost::PostVersion.new({account_id: 37, is_original: false, content: [PostBoost::PostContent.new]})]}) # PostInput | 

begin
  # Create post
  result = api_instance.create_post(workspace_uuid, post_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->create_post: #{e}"
end
```

#### Using the create_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Post>, Integer, Hash)> create_post_with_http_info(workspace_uuid, post_input)

```ruby
begin
  # Create post
  data, status_code, headers = api_instance.create_post_with_http_info(workspace_uuid, post_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Post>
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->create_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **post_input** | [**PostInput**](PostInput.md) |  |  |

### Return type

[**Post**](Post.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_post

> <DeleteResult> delete_post(workspace_uuid, post_uuid, opts)

Delete post

Deletes a post. Use `delete_mode` to control whether to also remove the published content from social platforms.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::PostsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
post_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the post.
opts = {
  delete_post_request: PostBoost::DeletePostRequest.new # DeletePostRequest | 
}

begin
  # Delete post
  result = api_instance.delete_post(workspace_uuid, post_uuid, opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->delete_post: #{e}"
end
```

#### Using the delete_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DeleteResult>, Integer, Hash)> delete_post_with_http_info(workspace_uuid, post_uuid, opts)

```ruby
begin
  # Delete post
  data, status_code, headers = api_instance.delete_post_with_http_info(workspace_uuid, post_uuid, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DeleteResult>
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->delete_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **post_uuid** | **String** | UUID of the post. |  |
| **delete_post_request** | [**DeletePostRequest**](DeletePostRequest.md) |  | [optional] |

### Return type

[**DeleteResult**](DeleteResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_posts_bulk

> <DeleteResult> delete_posts_bulk(workspace_uuid, delete_posts_bulk_request)

Delete posts (bulk)

Delete multiple posts at once.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::PostsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
delete_posts_bulk_request = PostBoost::DeletePostsBulkRequest.new({posts: ['posts_example']}) # DeletePostsBulkRequest | 

begin
  # Delete posts (bulk)
  result = api_instance.delete_posts_bulk(workspace_uuid, delete_posts_bulk_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->delete_posts_bulk: #{e}"
end
```

#### Using the delete_posts_bulk_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DeleteResult>, Integer, Hash)> delete_posts_bulk_with_http_info(workspace_uuid, delete_posts_bulk_request)

```ruby
begin
  # Delete posts (bulk)
  data, status_code, headers = api_instance.delete_posts_bulk_with_http_info(workspace_uuid, delete_posts_bulk_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DeleteResult>
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->delete_posts_bulk_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **delete_posts_bulk_request** | [**DeletePostsBulkRequest**](DeletePostsBulkRequest.md) |  |  |

### Return type

[**DeleteResult**](DeleteResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## get_post

> <Post> get_post(workspace_uuid, post_uuid)

Get post

Returns a single post with all its versions and associated accounts.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::PostsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
post_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the post.

begin
  # Get post
  result = api_instance.get_post(workspace_uuid, post_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->get_post: #{e}"
end
```

#### Using the get_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Post>, Integer, Hash)> get_post_with_http_info(workspace_uuid, post_uuid)

```ruby
begin
  # Get post
  data, status_code, headers = api_instance.get_post_with_http_info(workspace_uuid, post_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Post>
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->get_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **post_uuid** | **String** | UUID of the post. |  |

### Return type

[**Post**](Post.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_posts

> <ListPosts200Response> list_posts(workspace_uuid, opts)

List posts

Returns a paginated list of posts in the workspace.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::PostsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
opts = {
  page: 56 # Integer | 
}

begin
  # List posts
  result = api_instance.list_posts(workspace_uuid, opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->list_posts: #{e}"
end
```

#### Using the list_posts_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListPosts200Response>, Integer, Hash)> list_posts_with_http_info(workspace_uuid, opts)

```ruby
begin
  # List posts
  data, status_code, headers = api_instance.list_posts_with_http_info(workspace_uuid, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListPosts200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->list_posts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **page** | **Integer** |  | [optional][default to 1] |

### Return type

[**ListPosts200Response**](ListPosts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## schedule_post

> <ScheduleResult> schedule_post(workspace_uuid, post_uuid, schedule_post_request)

Schedule post

Schedule an existing post. Set `postNow: true` to publish immediately.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::PostsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
post_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the post.
schedule_post_request = PostBoost::SchedulePostRequest.new({post_now: false}) # SchedulePostRequest | 

begin
  # Schedule post
  result = api_instance.schedule_post(workspace_uuid, post_uuid, schedule_post_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->schedule_post: #{e}"
end
```

#### Using the schedule_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ScheduleResult>, Integer, Hash)> schedule_post_with_http_info(workspace_uuid, post_uuid, schedule_post_request)

```ruby
begin
  # Schedule post
  data, status_code, headers = api_instance.schedule_post_with_http_info(workspace_uuid, post_uuid, schedule_post_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ScheduleResult>
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->schedule_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **post_uuid** | **String** | UUID of the post. |  |
| **schedule_post_request** | [**SchedulePostRequest**](SchedulePostRequest.md) |  |  |

### Return type

[**ScheduleResult**](ScheduleResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_post

> Object update_post(workspace_uuid, post_uuid, post_input)

Update post

Replaces a post's versions, accounts, tags, and scheduling options. The post must not be in a published state.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::PostsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
post_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the post.
post_input = PostBoost::PostInput.new({versions: [PostBoost::PostVersion.new({account_id: 37, is_original: false, content: [PostBoost::PostContent.new]})]}) # PostInput | 

begin
  # Update post
  result = api_instance.update_post(workspace_uuid, post_uuid, post_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->update_post: #{e}"
end
```

#### Using the update_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> update_post_with_http_info(workspace_uuid, post_uuid, post_input)

```ruby
begin
  # Update post
  data, status_code, headers = api_instance.update_post_with_http_info(workspace_uuid, post_uuid, post_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->update_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **post_uuid** | **String** | UUID of the post. |  |
| **post_input** | [**PostInput**](PostInput.md) |  |  |

### Return type

**Object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

