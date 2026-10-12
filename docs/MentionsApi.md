# PostBoost::MentionsApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_mention**](MentionsApi.md#create_mention) | **POST** /{workspaceUuid}/mentions | Create mention |
| [**delete_mention**](MentionsApi.md#delete_mention) | **DELETE** /{workspaceUuid}/mentions/{mentionId} | Delete mention |
| [**get_mention**](MentionsApi.md#get_mention) | **GET** /{workspaceUuid}/mentions/{mentionId} | Get mention |
| [**list_mentions**](MentionsApi.md#list_mentions) | **GET** /{workspaceUuid}/mentions | List mentions |
| [**update_mention**](MentionsApi.md#update_mention) | **PUT** /{workspaceUuid}/mentions/{mentionId} | Update mention |


## create_mention

> <CreateMention201Response> create_mention(workspace_uuid, mention_input, opts)

Create mention

Adds a person or page to the mention book. When one of the submitted identities already belongs to a stored mention, that mention is reused and the identities are added to it (status `200` instead of `201`). 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::MentionsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
mention_input = PostBoost::MentionInput.new({name: 'name_example'}) # MentionInput | 
opts = {
  idempotency_key: 'idempotency_key_example' # String | Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with `Idempotent-Replayed: true` and has no further effect. Keys are scoped to your user, the workspace, the method and the path. 
}

begin
  # Create mention
  result = api_instance.create_mention(workspace_uuid, mention_input, opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling MentionsApi->create_mention: #{e}"
end
```

#### Using the create_mention_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateMention201Response>, Integer, Hash)> create_mention_with_http_info(workspace_uuid, mention_input, opts)

```ruby
begin
  # Create mention
  data, status_code, headers = api_instance.create_mention_with_http_info(workspace_uuid, mention_input, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateMention201Response>
rescue PostBoost::ApiError => e
  puts "Error when calling MentionsApi->create_mention_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **mention_input** | [**MentionInput**](MentionInput.md) |  |  |
| **idempotency_key** | **String** | Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with &#x60;Idempotent-Replayed: true&#x60; and has no further effect. Keys are scoped to your user, the workspace, the method and the path.  | [optional] |

### Return type

[**CreateMention201Response**](CreateMention201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_mention

> Object delete_mention(workspace_uuid, mention_id)

Delete mention

Removes a mention from the mention book. `success` is false when nothing was deleted.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::MentionsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
mention_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | The mention's `id` (a UUID).

begin
  # Delete mention
  result = api_instance.delete_mention(workspace_uuid, mention_id)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling MentionsApi->delete_mention: #{e}"
end
```

#### Using the delete_mention_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> delete_mention_with_http_info(workspace_uuid, mention_id)

```ruby
begin
  # Delete mention
  data, status_code, headers = api_instance.delete_mention_with_http_info(workspace_uuid, mention_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue PostBoost::ApiError => e
  puts "Error when calling MentionsApi->delete_mention_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **mention_id** | **String** | The mention&#39;s &#x60;id&#x60; (a UUID). |  |

### Return type

**Object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_mention

> <CreateMention201Response> get_mention(workspace_uuid, mention_id)

Get mention

Returns a single mention with its identities.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::MentionsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
mention_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | The mention's `id` (a UUID).

begin
  # Get mention
  result = api_instance.get_mention(workspace_uuid, mention_id)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling MentionsApi->get_mention: #{e}"
end
```

#### Using the get_mention_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateMention201Response>, Integer, Hash)> get_mention_with_http_info(workspace_uuid, mention_id)

```ruby
begin
  # Get mention
  data, status_code, headers = api_instance.get_mention_with_http_info(workspace_uuid, mention_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateMention201Response>
rescue PostBoost::ApiError => e
  puts "Error when calling MentionsApi->get_mention_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **mention_id** | **String** | The mention&#39;s &#x60;id&#x60; (a UUID). |  |

### Return type

[**CreateMention201Response**](CreateMention201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_mentions

> <ListMentions200Response> list_mentions(workspace_uuid, opts)

List mentions

Returns a paginated list of the workspace's mention book, ranked, with each entry's network identities.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::MentionsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
opts = {
  q: 'q_example', # String | Search keyword.
  per_page: 56, # Integer | 
  page: 56 # Integer | 
}

begin
  # List mentions
  result = api_instance.list_mentions(workspace_uuid, opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling MentionsApi->list_mentions: #{e}"
end
```

#### Using the list_mentions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListMentions200Response>, Integer, Hash)> list_mentions_with_http_info(workspace_uuid, opts)

```ruby
begin
  # List mentions
  data, status_code, headers = api_instance.list_mentions_with_http_info(workspace_uuid, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListMentions200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling MentionsApi->list_mentions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **q** | **String** | Search keyword. | [optional] |
| **per_page** | **Integer** |  | [optional][default to 25] |
| **page** | **Integer** |  | [optional][default to 1] |

### Return type

[**ListMentions200Response**](ListMentions200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_mention

> <CreateMention201Response> update_mention(workspace_uuid, mention_id, mention_input)

Update mention

Replaces the mention's name, avatar and identities. Identities for providers not in the payload are removed. An identity already held by another mention returns `422`.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::MentionsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
mention_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | The mention's `id` (a UUID).
mention_input = PostBoost::MentionInput.new({name: 'name_example'}) # MentionInput | 

begin
  # Update mention
  result = api_instance.update_mention(workspace_uuid, mention_id, mention_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling MentionsApi->update_mention: #{e}"
end
```

#### Using the update_mention_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateMention201Response>, Integer, Hash)> update_mention_with_http_info(workspace_uuid, mention_id, mention_input)

```ruby
begin
  # Update mention
  data, status_code, headers = api_instance.update_mention_with_http_info(workspace_uuid, mention_id, mention_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateMention201Response>
rescue PostBoost::ApiError => e
  puts "Error when calling MentionsApi->update_mention_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **mention_id** | **String** | The mention&#39;s &#x60;id&#x60; (a UUID). |  |
| **mention_input** | [**MentionInput**](MentionInput.md) |  |  |

### Return type

[**CreateMention201Response**](CreateMention201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

