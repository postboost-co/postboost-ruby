# PostBoost::PostsApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**add_post_to_queue**](PostsApi.md#add_post_to_queue) | **POST** /{workspaceUuid}/posts/add-to-queue/{postUuid} | Add post to queue |
| [**approve_post**](PostsApi.md#approve_post) | **POST** /{workspaceUuid}/posts/approve/{postUuid} | Approve post |
| [**create_post**](PostsApi.md#create_post) | **POST** /{workspaceUuid}/posts | Create post |
| [**create_recycling_rule**](PostsApi.md#create_recycling_rule) | **POST** /{workspaceUuid}/recycling-rules | Create a recycling rule |
| [**create_rss_feed**](PostsApi.md#create_rss_feed) | **POST** /{workspaceUuid}/rss-feeds | Add an RSS feed |
| [**delete_post**](PostsApi.md#delete_post) | **DELETE** /{workspaceUuid}/posts/{postUuid} | Delete post |
| [**delete_posts_bulk**](PostsApi.md#delete_posts_bulk) | **DELETE** /{workspaceUuid}/posts | Delete posts (bulk) |
| [**delete_recycling_rule**](PostsApi.md#delete_recycling_rule) | **DELETE** /{workspaceUuid}/recycling-rules/{ruleUuid} | Delete a recycling rule |
| [**delete_rss_feed**](PostsApi.md#delete_rss_feed) | **DELETE** /{workspaceUuid}/rss-feeds/{feedUuid} | Delete an RSS feed |
| [**get_post**](PostsApi.md#get_post) | **GET** /{workspaceUuid}/posts/{postUuid} | Get post |
| [**get_post_analytics**](PostsApi.md#get_post_analytics) | **GET** /{workspaceUuid}/posts/{postUuid}/analytics | Get post analytics |
| [**get_recycling_rule**](PostsApi.md#get_recycling_rule) | **GET** /{workspaceUuid}/recycling-rules/{ruleUuid} | Get a recycling rule |
| [**get_rss_feed**](PostsApi.md#get_rss_feed) | **GET** /{workspaceUuid}/rss-feeds/{feedUuid} | Get an RSS feed |
| [**list_posts**](PostsApi.md#list_posts) | **GET** /{workspaceUuid}/posts | List posts |
| [**list_recycling_rules**](PostsApi.md#list_recycling_rules) | **GET** /{workspaceUuid}/recycling-rules | List recycling rules |
| [**list_recycling_runs**](PostsApi.md#list_recycling_runs) | **GET** /{workspaceUuid}/recycling-rules/{ruleUuid}/runs | List a recycling rule&#39;s runs |
| [**list_rss_feeds**](PostsApi.md#list_rss_feeds) | **GET** /{workspaceUuid}/rss-feeds | List RSS feeds |
| [**poll_rss_feed**](PostsApi.md#poll_rss_feed) | **POST** /{workspaceUuid}/rss-feeds/{feedUuid}/poll | Check an RSS feed now |
| [**recycle_post**](PostsApi.md#recycle_post) | **POST** /{workspaceUuid}/posts/{postUuid}/recycle | Recycle a post on an interval |
| [**retry_post_account**](PostsApi.md#retry_post_account) | **POST** /{workspaceUuid}/posts/retry/{postUuid}/{accountUuid} | Retry publishing to one account |
| [**schedule_post**](PostsApi.md#schedule_post) | **POST** /{workspaceUuid}/posts/schedule/{postUuid} | Schedule post |
| [**update_post**](PostsApi.md#update_post) | **PUT** /{workspaceUuid}/posts/{postUuid} | Update post |
| [**update_recycling_rule**](PostsApi.md#update_recycling_rule) | **PUT** /{workspaceUuid}/recycling-rules/{ruleUuid} | Update, pause or resume a recycling rule |
| [**update_rss_feed**](PostsApi.md#update_rss_feed) | **PUT** /{workspaceUuid}/rss-feeds/{feedUuid} | Update, pause or resume an RSS feed |
| [**validate_post**](PostsApi.md#validate_post) | **POST** /{workspaceUuid}/posts/validate | Validate post (dry run) |


## add_post_to_queue

> <ScheduleResult> add_post_to_queue(workspace_uuid, post_uuid, opts)

Add post to queue

Add an existing post to the smart publishing queue. Each account of the post gets its own next free queue slot. Returns `422` when the post has no accounts, the posting schedule has no available times, or provider requirements are not met. 

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
  idempotency_key: 'idempotency_key_example', # String | Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with `Idempotent-Replayed: true` and has no further effect. Keys are scoped to your user, the workspace, the method and the path. 
  add_post_to_queue_request: PostBoost::AddPostToQueueRequest.new # AddPostToQueueRequest | 
}

begin
  # Add post to queue
  result = api_instance.add_post_to_queue(workspace_uuid, post_uuid, opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->add_post_to_queue: #{e}"
end
```

#### Using the add_post_to_queue_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ScheduleResult>, Integer, Hash)> add_post_to_queue_with_http_info(workspace_uuid, post_uuid, opts)

```ruby
begin
  # Add post to queue
  data, status_code, headers = api_instance.add_post_to_queue_with_http_info(workspace_uuid, post_uuid, opts)
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
| **idempotency_key** | **String** | Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with &#x60;Idempotent-Replayed: true&#x60; and has no further effect. Keys are scoped to your user, the workspace, the method and the path.  | [optional] |
| **add_post_to_queue_request** | [**AddPostToQueueRequest**](AddPostToQueueRequest.md) |  | [optional] |

### Return type

[**ScheduleResult**](ScheduleResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## approve_post

> <ScheduleResult> approve_post(workspace_uuid, post_uuid, opts)

Approve post

Approve a post that is pending review. The approver may move the post with `date`/`time` (read in `timezone`) and set per-account times with `accounts_schedule`; without them the post keeps the time it was submitted with. Provider requirements are validated and reported as `422`. 

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
  idempotency_key: 'idempotency_key_example', # String | Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with `Idempotent-Replayed: true` and has no further effect. Keys are scoped to your user, the workspace, the method and the path. 
  approve_post_request: PostBoost::ApprovePostRequest.new # ApprovePostRequest | 
}

begin
  # Approve post
  result = api_instance.approve_post(workspace_uuid, post_uuid, opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->approve_post: #{e}"
end
```

#### Using the approve_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ScheduleResult>, Integer, Hash)> approve_post_with_http_info(workspace_uuid, post_uuid, opts)

```ruby
begin
  # Approve post
  data, status_code, headers = api_instance.approve_post_with_http_info(workspace_uuid, post_uuid, opts)
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
| **idempotency_key** | **String** | Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with &#x60;Idempotent-Replayed: true&#x60; and has no further effect. Keys are scoped to your user, the workspace, the method and the path.  | [optional] |
| **approve_post_request** | [**ApprovePostRequest**](ApprovePostRequest.md) |  | [optional] |

### Return type

[**ScheduleResult**](ScheduleResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## create_post

> <Post> create_post(workspace_uuid, post_input, opts)

Create post

Create a new post. Use `schedule: true` with `date` and `time` to schedule, `schedule_now: true` to publish immediately, or `queue: true` to add to the smart publishing queue (each account gets its own queue slot).  `date`, `time` and `accounts_schedule` are read in `timezone` when given, otherwise in the workspace timezone. Use `accounts_schedule` to give individual accounts their own departure time.  Post bodies may reference mentions with `{{mention:<reference>}}` (see the Mentions endpoints). When the post is scheduled, provider requirements (for example a network that requires media) are validated up front and reported as `422`.  **First comment and threads.** A version's `content` is an ordered array. Item 0 is the post. Add a second item to publish a first comment on Facebook Page, Instagram and LinkedIn, or to continue a thread on X, Threads, Bluesky, Mastodon and Pixelfed:  ```json {   \"accounts\": [12],   \"schedule_now\": true,   \"versions\": [{     \"account_id\": 0,     \"is_original\": true,     \"content\": [       { \"body\": \"Our API 1.8 is live.\", \"media\": [345] },       { \"body\": \"Full changelog: https://postboost.co/docs/changelog/\" }     ]   }] } ```  The comment is posted right after the post goes live. If the comment fails, the post stays published and the account's entry on the post reports the error. 

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
opts = {
  idempotency_key: 'idempotency_key_example' # String | Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with `Idempotent-Replayed: true` and has no further effect. Keys are scoped to your user, the workspace, the method and the path. 
}

begin
  # Create post
  result = api_instance.create_post(workspace_uuid, post_input, opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->create_post: #{e}"
end
```

#### Using the create_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Post>, Integer, Hash)> create_post_with_http_info(workspace_uuid, post_input, opts)

```ruby
begin
  # Create post
  data, status_code, headers = api_instance.create_post_with_http_info(workspace_uuid, post_input, opts)
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
| **idempotency_key** | **String** | Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with &#x60;Idempotent-Replayed: true&#x60; and has no further effect. Keys are scoped to your user, the workspace, the method and the path.  | [optional] |

### Return type

[**Post**](Post.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## create_recycling_rule

> <CreateRecyclingRule201Response> create_recycling_rule(workspace_uuid, recycling_rule_input)

Create a recycling rule

Recycles one post (`post_uuid`) or a tag pool (`type: tag_pool` + `tag_uuid`) every `interval_days`. The first run is `start_at`, or one interval from now. Copies are never published immediately: `placement: queue` (default) takes each account's next free queue slot, `same_time` schedules at the source post's time of day, `draft` leaves a draft.  Copies pass the same guardrails as posts created through the API (duplicate guard, per-account daily caps, disconnected accounts, X monthly allowance). A refused copy is not created; the run is logged with the guard's code (see the runs endpoint). X accounts are left out of copies because X rejects repeated text. Admins and members only. 

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
recycling_rule_input = PostBoost::RecyclingRuleInput.new({interval_days: 37}) # RecyclingRuleInput | 

begin
  # Create a recycling rule
  result = api_instance.create_recycling_rule(workspace_uuid, recycling_rule_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->create_recycling_rule: #{e}"
end
```

#### Using the create_recycling_rule_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateRecyclingRule201Response>, Integer, Hash)> create_recycling_rule_with_http_info(workspace_uuid, recycling_rule_input)

```ruby
begin
  # Create a recycling rule
  data, status_code, headers = api_instance.create_recycling_rule_with_http_info(workspace_uuid, recycling_rule_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateRecyclingRule201Response>
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->create_recycling_rule_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **recycling_rule_input** | [**RecyclingRuleInput**](RecyclingRuleInput.md) |  |  |

### Return type

[**CreateRecyclingRule201Response**](CreateRecyclingRule201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## create_rss_feed

> <CreateRssFeed201Response> create_rss_feed(workspace_uuid, rss_feed_input)

Add an RSS feed

Checks the feed every 30 minutes and turns each item published after the feed was added into a post for `account_ids`: a draft (`mode: draft`, default) or a queued post (`mode: queue`). The text comes from `template` with `{title}`, `{link}` and `{summary}` placeholders. Each item becomes at most one post, at most `max_items_per_run` per check and 20 per workspace per day. Posts pass the same guardrails as API-created posts. Only public http(s) URLs are accepted. Admins and members only. 

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
rss_feed_input = PostBoost::RssFeedInput.new({url: 'url_example', account_ids: [37]}) # RssFeedInput | 

begin
  # Add an RSS feed
  result = api_instance.create_rss_feed(workspace_uuid, rss_feed_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->create_rss_feed: #{e}"
end
```

#### Using the create_rss_feed_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateRssFeed201Response>, Integer, Hash)> create_rss_feed_with_http_info(workspace_uuid, rss_feed_input)

```ruby
begin
  # Add an RSS feed
  data, status_code, headers = api_instance.create_rss_feed_with_http_info(workspace_uuid, rss_feed_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateRssFeed201Response>
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->create_rss_feed_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **rss_feed_input** | [**RssFeedInput**](RssFeedInput.md) |  |  |

### Return type

[**CreateRssFeed201Response**](CreateRssFeed201Response.md)

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


## delete_recycling_rule

> Object delete_recycling_rule(workspace_uuid, rule_uuid)

Delete a recycling rule

Deletes the rule and its run log. Copies it already created stay. Admins and members only.

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
rule_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the recycling rule.

begin
  # Delete a recycling rule
  result = api_instance.delete_recycling_rule(workspace_uuid, rule_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->delete_recycling_rule: #{e}"
end
```

#### Using the delete_recycling_rule_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> delete_recycling_rule_with_http_info(workspace_uuid, rule_uuid)

```ruby
begin
  # Delete a recycling rule
  data, status_code, headers = api_instance.delete_recycling_rule_with_http_info(workspace_uuid, rule_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->delete_recycling_rule_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **rule_uuid** | **String** | UUID of the recycling rule. |  |

### Return type

**Object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## delete_rss_feed

> Object delete_rss_feed(workspace_uuid, feed_uuid)

Delete an RSS feed

Stops the feed. Posts it already created stay. Admins and members only.

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
feed_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the RSS feed.

begin
  # Delete an RSS feed
  result = api_instance.delete_rss_feed(workspace_uuid, feed_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->delete_rss_feed: #{e}"
end
```

#### Using the delete_rss_feed_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> delete_rss_feed_with_http_info(workspace_uuid, feed_uuid)

```ruby
begin
  # Delete an RSS feed
  data, status_code, headers = api_instance.delete_rss_feed_with_http_info(workspace_uuid, feed_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->delete_rss_feed_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **feed_uuid** | **String** | UUID of the RSS feed. |  |

### Return type

**Object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
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


## get_post_analytics

> <PostAnalytics> get_post_analytics(workspace_uuid, post_uuid)

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

api_instance = PostBoost::PostsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
post_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the post.

begin
  # Get post analytics
  result = api_instance.get_post_analytics(workspace_uuid, post_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->get_post_analytics: #{e}"
end
```

#### Using the get_post_analytics_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PostAnalytics>, Integer, Hash)> get_post_analytics_with_http_info(workspace_uuid, post_uuid)

```ruby
begin
  # Get post analytics
  data, status_code, headers = api_instance.get_post_analytics_with_http_info(workspace_uuid, post_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PostAnalytics>
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->get_post_analytics_with_http_info: #{e}"
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


## get_recycling_rule

> <CreateRecyclingRule201Response> get_recycling_rule(workspace_uuid, rule_uuid)

Get a recycling rule

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
rule_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the recycling rule.

begin
  # Get a recycling rule
  result = api_instance.get_recycling_rule(workspace_uuid, rule_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->get_recycling_rule: #{e}"
end
```

#### Using the get_recycling_rule_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateRecyclingRule201Response>, Integer, Hash)> get_recycling_rule_with_http_info(workspace_uuid, rule_uuid)

```ruby
begin
  # Get a recycling rule
  data, status_code, headers = api_instance.get_recycling_rule_with_http_info(workspace_uuid, rule_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateRecyclingRule201Response>
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->get_recycling_rule_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **rule_uuid** | **String** | UUID of the recycling rule. |  |

### Return type

[**CreateRecyclingRule201Response**](CreateRecyclingRule201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_rss_feed

> <CreateRssFeed201Response> get_rss_feed(workspace_uuid, feed_uuid)

Get an RSS feed

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
feed_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the RSS feed.

begin
  # Get an RSS feed
  result = api_instance.get_rss_feed(workspace_uuid, feed_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->get_rss_feed: #{e}"
end
```

#### Using the get_rss_feed_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateRssFeed201Response>, Integer, Hash)> get_rss_feed_with_http_info(workspace_uuid, feed_uuid)

```ruby
begin
  # Get an RSS feed
  data, status_code, headers = api_instance.get_rss_feed_with_http_info(workspace_uuid, feed_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateRssFeed201Response>
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->get_rss_feed_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **feed_uuid** | **String** | UUID of the RSS feed. |  |

### Return type

[**CreateRssFeed201Response**](CreateRssFeed201Response.md)

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


## list_recycling_rules

> <ListRecyclingRules200Response> list_recycling_rules(workspace_uuid)

List recycling rules

Evergreen recycling rules of the workspace, newest first. A rule copies a post (or the least recently recycled published post with a tag) every `interval_days` and places the copy in the queue. Copies are ordinary posts: they show in the calendar and the queue. 

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

begin
  # List recycling rules
  result = api_instance.list_recycling_rules(workspace_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->list_recycling_rules: #{e}"
end
```

#### Using the list_recycling_rules_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListRecyclingRules200Response>, Integer, Hash)> list_recycling_rules_with_http_info(workspace_uuid)

```ruby
begin
  # List recycling rules
  data, status_code, headers = api_instance.list_recycling_rules_with_http_info(workspace_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListRecyclingRules200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->list_recycling_rules_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |

### Return type

[**ListRecyclingRules200Response**](ListRecyclingRules200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_recycling_runs

> <ListRecyclingRuns200Response> list_recycling_runs(workspace_uuid, rule_uuid)

List a recycling rule's runs

The latest 100 runs of the rule, newest first: the copy each run created, or why it skipped (`source_unavailable`, `no_eligible_post`, `no_accounts`, `queue_full`, `x_skipped_identical_text`, or a guardrail code such as `duplicate_post` or `account_daily_cap_reached`). 

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
rule_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the recycling rule.

begin
  # List a recycling rule's runs
  result = api_instance.list_recycling_runs(workspace_uuid, rule_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->list_recycling_runs: #{e}"
end
```

#### Using the list_recycling_runs_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListRecyclingRuns200Response>, Integer, Hash)> list_recycling_runs_with_http_info(workspace_uuid, rule_uuid)

```ruby
begin
  # List a recycling rule's runs
  data, status_code, headers = api_instance.list_recycling_runs_with_http_info(workspace_uuid, rule_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListRecyclingRuns200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->list_recycling_runs_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **rule_uuid** | **String** | UUID of the recycling rule. |  |

### Return type

[**ListRecyclingRuns200Response**](ListRecyclingRuns200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_rss_feeds

> <ListRssFeeds200Response> list_rss_feeds(workspace_uuid)

List RSS feeds

RSS and Atom feeds whose new items become posts, newest first.

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

begin
  # List RSS feeds
  result = api_instance.list_rss_feeds(workspace_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->list_rss_feeds: #{e}"
end
```

#### Using the list_rss_feeds_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListRssFeeds200Response>, Integer, Hash)> list_rss_feeds_with_http_info(workspace_uuid)

```ruby
begin
  # List RSS feeds
  data, status_code, headers = api_instance.list_rss_feeds_with_http_info(workspace_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListRssFeeds200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->list_rss_feeds_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |

### Return type

[**ListRssFeeds200Response**](ListRssFeeds200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## poll_rss_feed

> <PollRssFeed200Response> poll_rss_feed(workspace_uuid, feed_uuid)

Check an RSS feed now

Reads the feed immediately instead of waiting for the next check. Limited to 6 calls per minute. Admins and members only.

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
feed_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the RSS feed.

begin
  # Check an RSS feed now
  result = api_instance.poll_rss_feed(workspace_uuid, feed_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->poll_rss_feed: #{e}"
end
```

#### Using the poll_rss_feed_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PollRssFeed200Response>, Integer, Hash)> poll_rss_feed_with_http_info(workspace_uuid, feed_uuid)

```ruby
begin
  # Check an RSS feed now
  data, status_code, headers = api_instance.poll_rss_feed_with_http_info(workspace_uuid, feed_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PollRssFeed200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->poll_rss_feed_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **feed_uuid** | **String** | UUID of the RSS feed. |  |

### Return type

[**PollRssFeed200Response**](PollRssFeed200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## recycle_post

> <CreateRecyclingRule201Response> recycle_post(workspace_uuid, post_uuid, recycling_rule_settings)

Recycle a post on an interval

Shortcut for creating a `post` recycling rule for this post. Same body as `createRecyclingRule` without `type`, `post_uuid` and `tag_uuid`. Admins and members only. 

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
recycling_rule_settings = PostBoost::RecyclingRuleSettings.new({interval_days: 37}) # RecyclingRuleSettings | 

begin
  # Recycle a post on an interval
  result = api_instance.recycle_post(workspace_uuid, post_uuid, recycling_rule_settings)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->recycle_post: #{e}"
end
```

#### Using the recycle_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateRecyclingRule201Response>, Integer, Hash)> recycle_post_with_http_info(workspace_uuid, post_uuid, recycling_rule_settings)

```ruby
begin
  # Recycle a post on an interval
  data, status_code, headers = api_instance.recycle_post_with_http_info(workspace_uuid, post_uuid, recycling_rule_settings)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateRecyclingRule201Response>
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->recycle_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **post_uuid** | **String** | UUID of the post. |  |
| **recycling_rule_settings** | [**RecyclingRuleSettings**](RecyclingRuleSettings.md) |  |  |

### Return type

[**CreateRecyclingRule201Response**](CreateRecyclingRule201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## retry_post_account

> <RetryPostAccountResult> retry_post_account(workspace_uuid, post_uuid, account_uuid, opts)

Retry publishing to one account

Re-publishes a post to a single account whose publishing failed. Returns `422` when the account is not on the post, the post is still publishing, or the account did not fail.

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
account_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the social media account.
opts = {
  idempotency_key: 'idempotency_key_example' # String | Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with `Idempotent-Replayed: true` and has no further effect. Keys are scoped to your user, the workspace, the method and the path. 
}

begin
  # Retry publishing to one account
  result = api_instance.retry_post_account(workspace_uuid, post_uuid, account_uuid, opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->retry_post_account: #{e}"
end
```

#### Using the retry_post_account_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<RetryPostAccountResult>, Integer, Hash)> retry_post_account_with_http_info(workspace_uuid, post_uuid, account_uuid, opts)

```ruby
begin
  # Retry publishing to one account
  data, status_code, headers = api_instance.retry_post_account_with_http_info(workspace_uuid, post_uuid, account_uuid, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <RetryPostAccountResult>
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->retry_post_account_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **post_uuid** | **String** | UUID of the post. |  |
| **account_uuid** | **String** | UUID of the social media account. |  |
| **idempotency_key** | **String** | Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with &#x60;Idempotent-Replayed: true&#x60; and has no further effect. Keys are scoped to your user, the workspace, the method and the path.  | [optional] |

### Return type

[**RetryPostAccountResult**](RetryPostAccountResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## schedule_post

> <ScheduleResult> schedule_post(workspace_uuid, post_uuid, schedule_post_request, opts)

Schedule post

Schedule an existing post. Optionally move it with `date`/`time` (read in `timezone`) and give accounts their own times with `accounts_schedule`. Set `postNow: true` to publish immediately; publishing starts within the request and any per-account times are dropped. Provider requirements are validated and reported as `422`. 

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
opts = {
  idempotency_key: 'idempotency_key_example' # String | Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with `Idempotent-Replayed: true` and has no further effect. Keys are scoped to your user, the workspace, the method and the path. 
}

begin
  # Schedule post
  result = api_instance.schedule_post(workspace_uuid, post_uuid, schedule_post_request, opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->schedule_post: #{e}"
end
```

#### Using the schedule_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ScheduleResult>, Integer, Hash)> schedule_post_with_http_info(workspace_uuid, post_uuid, schedule_post_request, opts)

```ruby
begin
  # Schedule post
  data, status_code, headers = api_instance.schedule_post_with_http_info(workspace_uuid, post_uuid, schedule_post_request, opts)
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
| **idempotency_key** | **String** | Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with &#x60;Idempotent-Replayed: true&#x60; and has no further effect. Keys are scoped to your user, the workspace, the method and the path.  | [optional] |

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

Replaces a post's versions, accounts, tags, and scheduling options. The post must not be in a published state. `timezone` is honoured: `date`, `time` and `accounts_schedule` are read in it. When the post stays scheduled, provider requirements are validated and reported as `422`. 

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


## update_recycling_rule

> <CreateRecyclingRule201Response> update_recycling_rule(workspace_uuid, rule_uuid, recycling_rule_update)

Update, pause or resume a recycling rule

Changes the interval, limit, placement or accounts, or pauses (`active: false`) and resumes the rule. Fields you leave out keep their value. A rule that reached `max_runs` resumes only with a higher `max_runs`. Admins and members only. 

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
rule_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the recycling rule.
recycling_rule_update = PostBoost::RecyclingRuleUpdate.new # RecyclingRuleUpdate | 

begin
  # Update, pause or resume a recycling rule
  result = api_instance.update_recycling_rule(workspace_uuid, rule_uuid, recycling_rule_update)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->update_recycling_rule: #{e}"
end
```

#### Using the update_recycling_rule_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateRecyclingRule201Response>, Integer, Hash)> update_recycling_rule_with_http_info(workspace_uuid, rule_uuid, recycling_rule_update)

```ruby
begin
  # Update, pause or resume a recycling rule
  data, status_code, headers = api_instance.update_recycling_rule_with_http_info(workspace_uuid, rule_uuid, recycling_rule_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateRecyclingRule201Response>
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->update_recycling_rule_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **rule_uuid** | **String** | UUID of the recycling rule. |  |
| **recycling_rule_update** | [**RecyclingRuleUpdate**](RecyclingRuleUpdate.md) |  |  |

### Return type

[**CreateRecyclingRule201Response**](CreateRecyclingRule201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_rss_feed

> <CreateRssFeed201Response> update_rss_feed(workspace_uuid, feed_uuid, rss_feed_update)

Update, pause or resume an RSS feed

Fields you leave out keep their value. Resuming (`active: true`) clears the error backoff. Admins and members only.

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
feed_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the RSS feed.
rss_feed_update = PostBoost::RssFeedUpdate.new # RssFeedUpdate | 

begin
  # Update, pause or resume an RSS feed
  result = api_instance.update_rss_feed(workspace_uuid, feed_uuid, rss_feed_update)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->update_rss_feed: #{e}"
end
```

#### Using the update_rss_feed_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateRssFeed201Response>, Integer, Hash)> update_rss_feed_with_http_info(workspace_uuid, feed_uuid, rss_feed_update)

```ruby
begin
  # Update, pause or resume an RSS feed
  data, status_code, headers = api_instance.update_rss_feed_with_http_info(workspace_uuid, feed_uuid, rss_feed_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateRssFeed201Response>
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->update_rss_feed_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **feed_uuid** | **String** | UUID of the RSS feed. |  |
| **rss_feed_update** | [**RssFeedUpdate**](RssFeedUpdate.md) |  |  |

### Return type

[**CreateRssFeed201Response**](CreateRssFeed201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## validate_post

> <PreflightResult> validate_post(workspace_uuid, post_input)

Validate post (dry run)

Runs everything create-post checks without creating anything: request validation, network requirements (text length, media count and type, links) for every given account, whether or not the post is scheduled, and the guardrails (duplicate content, daily caps, account health). Always answers `200`; read `valid`. Any workspace member, including viewers, may call it. Recommended agent loop: account health, validate, then create. 

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
  # Validate post (dry run)
  result = api_instance.validate_post(workspace_uuid, post_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->validate_post: #{e}"
end
```

#### Using the validate_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PreflightResult>, Integer, Hash)> validate_post_with_http_info(workspace_uuid, post_input)

```ruby
begin
  # Validate post (dry run)
  data, status_code, headers = api_instance.validate_post_with_http_info(workspace_uuid, post_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PreflightResult>
rescue PostBoost::ApiError => e
  puts "Error when calling PostsApi->validate_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **post_input** | [**PostInput**](PostInput.md) |  |  |

### Return type

[**PreflightResult**](PreflightResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

