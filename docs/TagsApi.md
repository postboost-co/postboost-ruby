# PostBoost::TagsApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_tag**](TagsApi.md#create_tag) | **POST** /{workspaceUuid}/tags | Create tag |
| [**delete_tag**](TagsApi.md#delete_tag) | **DELETE** /{workspaceUuid}/tags/{tagUuid} | Delete tag |
| [**get_tag**](TagsApi.md#get_tag) | **GET** /{workspaceUuid}/tags/{tagUuid} | Get tag |
| [**list_tags**](TagsApi.md#list_tags) | **GET** /{workspaceUuid}/tags | List tags |
| [**update_tag**](TagsApi.md#update_tag) | **PUT** /{workspaceUuid}/tags/{tagUuid} | Update tag |


## create_tag

> <Tag> create_tag(workspace_uuid, tag_input)

Create tag

Creates a new color-coded tag in the workspace for organizing posts.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::TagsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
tag_input = PostBoost::TagInput.new({name: 'name_example', hex_color: '#3B82F6'}) # TagInput | 

begin
  # Create tag
  result = api_instance.create_tag(workspace_uuid, tag_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling TagsApi->create_tag: #{e}"
end
```

#### Using the create_tag_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Tag>, Integer, Hash)> create_tag_with_http_info(workspace_uuid, tag_input)

```ruby
begin
  # Create tag
  data, status_code, headers = api_instance.create_tag_with_http_info(workspace_uuid, tag_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Tag>
rescue PostBoost::ApiError => e
  puts "Error when calling TagsApi->create_tag_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **tag_input** | [**TagInput**](TagInput.md) |  |  |

### Return type

[**Tag**](Tag.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_tag

> Object delete_tag(workspace_uuid, tag_uuid)

Delete tag

Permanently deletes a tag. Posts that had this tag attached are unaffected.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::TagsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
tag_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the tag.

begin
  # Delete tag
  result = api_instance.delete_tag(workspace_uuid, tag_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling TagsApi->delete_tag: #{e}"
end
```

#### Using the delete_tag_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> delete_tag_with_http_info(workspace_uuid, tag_uuid)

```ruby
begin
  # Delete tag
  data, status_code, headers = api_instance.delete_tag_with_http_info(workspace_uuid, tag_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue PostBoost::ApiError => e
  puts "Error when calling TagsApi->delete_tag_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **tag_uuid** | **String** | UUID of the tag. |  |

### Return type

**Object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_tag

> <Tag> get_tag(workspace_uuid, tag_uuid)

Get tag

Returns a single tag by UUID.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::TagsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
tag_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the tag.

begin
  # Get tag
  result = api_instance.get_tag(workspace_uuid, tag_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling TagsApi->get_tag: #{e}"
end
```

#### Using the get_tag_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Tag>, Integer, Hash)> get_tag_with_http_info(workspace_uuid, tag_uuid)

```ruby
begin
  # Get tag
  data, status_code, headers = api_instance.get_tag_with_http_info(workspace_uuid, tag_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Tag>
rescue PostBoost::ApiError => e
  puts "Error when calling TagsApi->get_tag_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **tag_uuid** | **String** | UUID of the tag. |  |

### Return type

[**Tag**](Tag.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_tags

> <ListTags200Response> list_tags(workspace_uuid)

List tags

Returns all tags defined in the workspace.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::TagsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.

begin
  # List tags
  result = api_instance.list_tags(workspace_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling TagsApi->list_tags: #{e}"
end
```

#### Using the list_tags_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListTags200Response>, Integer, Hash)> list_tags_with_http_info(workspace_uuid)

```ruby
begin
  # List tags
  data, status_code, headers = api_instance.list_tags_with_http_info(workspace_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListTags200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling TagsApi->list_tags_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |

### Return type

[**ListTags200Response**](ListTags200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_tag

> Object update_tag(workspace_uuid, tag_uuid, tag_input)

Update tag

Updates a tag's name or color.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::TagsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
tag_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the tag.
tag_input = PostBoost::TagInput.new({name: 'name_example', hex_color: '#3B82F6'}) # TagInput | 

begin
  # Update tag
  result = api_instance.update_tag(workspace_uuid, tag_uuid, tag_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling TagsApi->update_tag: #{e}"
end
```

#### Using the update_tag_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> update_tag_with_http_info(workspace_uuid, tag_uuid, tag_input)

```ruby
begin
  # Update tag
  data, status_code, headers = api_instance.update_tag_with_http_info(workspace_uuid, tag_uuid, tag_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue PostBoost::ApiError => e
  puts "Error when calling TagsApi->update_tag_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **tag_uuid** | **String** | UUID of the tag. |  |
| **tag_input** | [**TagInput**](TagInput.md) |  |  |

### Return type

**Object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

