# PostBoost::AccountGroupsApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_account_group**](AccountGroupsApi.md#create_account_group) | **POST** /{workspaceUuid}/account-groups | Create an account group |
| [**delete_account_group**](AccountGroupsApi.md#delete_account_group) | **DELETE** /{workspaceUuid}/account-groups/{accountGroupUuid} | Delete an account group |
| [**get_account_group**](AccountGroupsApi.md#get_account_group) | **GET** /{workspaceUuid}/account-groups/{accountGroupUuid} | Get an account group |
| [**list_account_groups**](AccountGroupsApi.md#list_account_groups) | **GET** /{workspaceUuid}/account-groups | List account groups |
| [**update_account_group**](AccountGroupsApi.md#update_account_group) | **PUT** /{workspaceUuid}/account-groups/{accountGroupUuid} | Update an account group |


## create_account_group

> <CreateAccountGroup201Response> create_account_group(workspace_uuid, account_group_input)

Create an account group

Creates a named set of accounts of this workspace. Admins and members only (not viewers). 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::AccountGroupsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
account_group_input = PostBoost::AccountGroupInput.new({name: 'name_example'}) # AccountGroupInput | 

begin
  # Create an account group
  result = api_instance.create_account_group(workspace_uuid, account_group_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AccountGroupsApi->create_account_group: #{e}"
end
```

#### Using the create_account_group_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateAccountGroup201Response>, Integer, Hash)> create_account_group_with_http_info(workspace_uuid, account_group_input)

```ruby
begin
  # Create an account group
  data, status_code, headers = api_instance.create_account_group_with_http_info(workspace_uuid, account_group_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateAccountGroup201Response>
rescue PostBoost::ApiError => e
  puts "Error when calling AccountGroupsApi->create_account_group_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **account_group_input** | [**AccountGroupInput**](AccountGroupInput.md) |  |  |

### Return type

[**CreateAccountGroup201Response**](CreateAccountGroup201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_account_group

> delete_account_group(workspace_uuid, account_group_uuid)

Delete an account group

Deletes the group, not its accounts. Admins and members only (not viewers). 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::AccountGroupsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
account_group_uuid = 'account_group_uuid_example' # String | The account group `uuid`.

begin
  # Delete an account group
  api_instance.delete_account_group(workspace_uuid, account_group_uuid)
rescue PostBoost::ApiError => e
  puts "Error when calling AccountGroupsApi->delete_account_group: #{e}"
end
```

#### Using the delete_account_group_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_account_group_with_http_info(workspace_uuid, account_group_uuid)

```ruby
begin
  # Delete an account group
  data, status_code, headers = api_instance.delete_account_group_with_http_info(workspace_uuid, account_group_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue PostBoost::ApiError => e
  puts "Error when calling AccountGroupsApi->delete_account_group_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **account_group_uuid** | **String** | The account group &#x60;uuid&#x60;. |  |

### Return type

nil (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_account_group

> <CreateAccountGroup201Response> get_account_group(workspace_uuid, account_group_uuid)

Get an account group

One account group. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::AccountGroupsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
account_group_uuid = 'account_group_uuid_example' # String | The account group `uuid`.

begin
  # Get an account group
  result = api_instance.get_account_group(workspace_uuid, account_group_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AccountGroupsApi->get_account_group: #{e}"
end
```

#### Using the get_account_group_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateAccountGroup201Response>, Integer, Hash)> get_account_group_with_http_info(workspace_uuid, account_group_uuid)

```ruby
begin
  # Get an account group
  data, status_code, headers = api_instance.get_account_group_with_http_info(workspace_uuid, account_group_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateAccountGroup201Response>
rescue PostBoost::ApiError => e
  puts "Error when calling AccountGroupsApi->get_account_group_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **account_group_uuid** | **String** | The account group &#x60;uuid&#x60;. |  |

### Return type

[**CreateAccountGroup201Response**](CreateAccountGroup201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_account_groups

> <ListAccountGroups200Response> list_account_groups(workspace_uuid, opts)

List account groups

Named sets of accounts, sorted by name, with their account ids. Pass `account_ids` as `accounts` when you create a post to publish to the whole group. Paginated with `page` and `per_page` (default 100). A key limited to some accounts only sees groups whose accounts are all among its accounts, and `meta.total` counts only those. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::AccountGroupsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
opts = {
  page: 56, # Integer | Page number (1-based).
  per_page: 56 # Integer | Items per page, 1-100.
}

begin
  # List account groups
  result = api_instance.list_account_groups(workspace_uuid, opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AccountGroupsApi->list_account_groups: #{e}"
end
```

#### Using the list_account_groups_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListAccountGroups200Response>, Integer, Hash)> list_account_groups_with_http_info(workspace_uuid, opts)

```ruby
begin
  # List account groups
  data, status_code, headers = api_instance.list_account_groups_with_http_info(workspace_uuid, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListAccountGroups200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling AccountGroupsApi->list_account_groups_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **page** | **Integer** | Page number (1-based). | [optional][default to 1] |
| **per_page** | **Integer** | Items per page, 1-100. | [optional][default to 100] |

### Return type

[**ListAccountGroups200Response**](ListAccountGroups200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_account_group

> <CreateAccountGroup201Response> update_account_group(workspace_uuid, account_group_uuid, account_group_input)

Update an account group

Replaces the name and the accounts of the group (accounts you leave out are removed). Admins and members only (not viewers). 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::AccountGroupsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
account_group_uuid = 'account_group_uuid_example' # String | The account group `uuid`.
account_group_input = PostBoost::AccountGroupInput.new({name: 'name_example'}) # AccountGroupInput | 

begin
  # Update an account group
  result = api_instance.update_account_group(workspace_uuid, account_group_uuid, account_group_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AccountGroupsApi->update_account_group: #{e}"
end
```

#### Using the update_account_group_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateAccountGroup201Response>, Integer, Hash)> update_account_group_with_http_info(workspace_uuid, account_group_uuid, account_group_input)

```ruby
begin
  # Update an account group
  data, status_code, headers = api_instance.update_account_group_with_http_info(workspace_uuid, account_group_uuid, account_group_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateAccountGroup201Response>
rescue PostBoost::ApiError => e
  puts "Error when calling AccountGroupsApi->update_account_group_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **account_group_uuid** | **String** | The account group &#x60;uuid&#x60;. |  |
| **account_group_input** | [**AccountGroupInput**](AccountGroupInput.md) |  |  |

### Return type

[**CreateAccountGroup201Response**](CreateAccountGroup201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

