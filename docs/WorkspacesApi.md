# PostBoost::WorkspacesApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**add_user_to_workspace**](WorkspacesApi.md#add_user_to_workspace) | **POST** /panel/workspaces/{workspaceUuid}/users | Add user to workspace |
| [**create_workspace**](WorkspacesApi.md#create_workspace) | **POST** /panel/workspaces | Create workspace |
| [**delete_workspace**](WorkspacesApi.md#delete_workspace) | **DELETE** /panel/workspaces/{workspaceUuid} | Delete workspace |
| [**delete_workspaces_bulk**](WorkspacesApi.md#delete_workspaces_bulk) | **DELETE** /panel/workspaces | Delete workspaces (bulk) |
| [**get_workspace**](WorkspacesApi.md#get_workspace) | **GET** /panel/workspaces/{workspaceUuid} | Get workspace |
| [**list_workspaces**](WorkspacesApi.md#list_workspaces) | **GET** /panel/workspaces | List workspaces |
| [**remove_user_from_workspace**](WorkspacesApi.md#remove_user_from_workspace) | **DELETE** /panel/workspaces/{workspaceUuid}/users | Remove user from workspace |
| [**update_workspace**](WorkspacesApi.md#update_workspace) | **PUT** /panel/workspaces/{workspaceUuid} | Update workspace |
| [**update_workspace_user**](WorkspacesApi.md#update_workspace_user) | **PUT** /panel/workspaces/{workspaceUuid}/users | Update user role in workspace |


## add_user_to_workspace

> Object add_user_to_workspace(workspace_uuid, workspace_user_input)

Add user to workspace

Adds an existing user to the workspace with a specified role. Admin only.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::WorkspacesApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
workspace_user_input = PostBoost::WorkspaceUserInput.new({user_id: 37, role: 'admin', can_approve: false, is_owner: false}) # WorkspaceUserInput | 

begin
  # Add user to workspace
  result = api_instance.add_user_to_workspace(workspace_uuid, workspace_user_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling WorkspacesApi->add_user_to_workspace: #{e}"
end
```

#### Using the add_user_to_workspace_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> add_user_to_workspace_with_http_info(workspace_uuid, workspace_user_input)

```ruby
begin
  # Add user to workspace
  data, status_code, headers = api_instance.add_user_to_workspace_with_http_info(workspace_uuid, workspace_user_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue PostBoost::ApiError => e
  puts "Error when calling WorkspacesApi->add_user_to_workspace_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **workspace_user_input** | [**WorkspaceUserInput**](WorkspaceUserInput.md) |  |  |

### Return type

**Object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## create_workspace

> <Workspace> create_workspace(workspace_input)

Create workspace

Create a new workspace. Admin only.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::WorkspacesApi.new
workspace_input = PostBoost::WorkspaceInput.new({name: 'name_example', hex_color: '#1d4ed8', access_status: 'subscription'}) # WorkspaceInput | 

begin
  # Create workspace
  result = api_instance.create_workspace(workspace_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling WorkspacesApi->create_workspace: #{e}"
end
```

#### Using the create_workspace_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Workspace>, Integer, Hash)> create_workspace_with_http_info(workspace_input)

```ruby
begin
  # Create workspace
  data, status_code, headers = api_instance.create_workspace_with_http_info(workspace_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Workspace>
rescue PostBoost::ApiError => e
  puts "Error when calling WorkspacesApi->create_workspace_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_input** | [**WorkspaceInput**](WorkspaceInput.md) |  |  |

### Return type

[**Workspace**](Workspace.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_workspace

> Object delete_workspace(workspace_uuid)

Delete workspace

Permanently deletes a single workspace and all its associated data. Admin only.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::WorkspacesApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.

begin
  # Delete workspace
  result = api_instance.delete_workspace(workspace_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling WorkspacesApi->delete_workspace: #{e}"
end
```

#### Using the delete_workspace_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> delete_workspace_with_http_info(workspace_uuid)

```ruby
begin
  # Delete workspace
  data, status_code, headers = api_instance.delete_workspace_with_http_info(workspace_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue PostBoost::ApiError => e
  puts "Error when calling WorkspacesApi->delete_workspace_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |

### Return type

**Object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## delete_workspaces_bulk

> Object delete_workspaces_bulk(delete_workspaces_bulk_request)

Delete workspaces (bulk)

Permanently deletes one or more workspaces and all their associated data. Admin only.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::WorkspacesApi.new
delete_workspaces_bulk_request = PostBoost::DeleteWorkspacesBulkRequest.new({workspaces: ['workspaces_example']}) # DeleteWorkspacesBulkRequest | 

begin
  # Delete workspaces (bulk)
  result = api_instance.delete_workspaces_bulk(delete_workspaces_bulk_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling WorkspacesApi->delete_workspaces_bulk: #{e}"
end
```

#### Using the delete_workspaces_bulk_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> delete_workspaces_bulk_with_http_info(delete_workspaces_bulk_request)

```ruby
begin
  # Delete workspaces (bulk)
  data, status_code, headers = api_instance.delete_workspaces_bulk_with_http_info(delete_workspaces_bulk_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue PostBoost::ApiError => e
  puts "Error when calling WorkspacesApi->delete_workspaces_bulk_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **delete_workspaces_bulk_request** | [**DeleteWorkspacesBulkRequest**](DeleteWorkspacesBulkRequest.md) |  |  |

### Return type

**Object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## get_workspace

> <Workspace> get_workspace(workspace_uuid)

Get workspace

Returns a single workspace by UUID including its subscription status. Admin only.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::WorkspacesApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.

begin
  # Get workspace
  result = api_instance.get_workspace(workspace_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling WorkspacesApi->get_workspace: #{e}"
end
```

#### Using the get_workspace_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Workspace>, Integer, Hash)> get_workspace_with_http_info(workspace_uuid)

```ruby
begin
  # Get workspace
  data, status_code, headers = api_instance.get_workspace_with_http_info(workspace_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Workspace>
rescue PostBoost::ApiError => e
  puts "Error when calling WorkspacesApi->get_workspace_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |

### Return type

[**Workspace**](Workspace.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_workspaces

> <ListWorkspaces200Response> list_workspaces(opts)

List workspaces

Returns a paginated list of all workspaces. Admin only.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::WorkspacesApi.new
opts = {
  keyword: 'keyword_example', # String | 
  subscription_status: 'active', # String | 
  access_status: 'subscription', # String | 
  page: 56 # Integer | Page number (15 items per page).
}

begin
  # List workspaces
  result = api_instance.list_workspaces(opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling WorkspacesApi->list_workspaces: #{e}"
end
```

#### Using the list_workspaces_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListWorkspaces200Response>, Integer, Hash)> list_workspaces_with_http_info(opts)

```ruby
begin
  # List workspaces
  data, status_code, headers = api_instance.list_workspaces_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListWorkspaces200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling WorkspacesApi->list_workspaces_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **keyword** | **String** |  | [optional] |
| **subscription_status** | **String** |  | [optional] |
| **access_status** | **String** |  | [optional] |
| **page** | **Integer** | Page number (15 items per page). | [optional][default to 1] |

### Return type

[**ListWorkspaces200Response**](ListWorkspaces200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## remove_user_from_workspace

> Object remove_user_from_workspace(workspace_uuid, remove_user_from_workspace_request)

Remove user from workspace

Removes a user's access to the workspace. The user account is not deleted. Admin only.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::WorkspacesApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
remove_user_from_workspace_request = PostBoost::RemoveUserFromWorkspaceRequest.new({user_id: 37}) # RemoveUserFromWorkspaceRequest | 

begin
  # Remove user from workspace
  result = api_instance.remove_user_from_workspace(workspace_uuid, remove_user_from_workspace_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling WorkspacesApi->remove_user_from_workspace: #{e}"
end
```

#### Using the remove_user_from_workspace_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> remove_user_from_workspace_with_http_info(workspace_uuid, remove_user_from_workspace_request)

```ruby
begin
  # Remove user from workspace
  data, status_code, headers = api_instance.remove_user_from_workspace_with_http_info(workspace_uuid, remove_user_from_workspace_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue PostBoost::ApiError => e
  puts "Error when calling WorkspacesApi->remove_user_from_workspace_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **remove_user_from_workspace_request** | [**RemoveUserFromWorkspaceRequest**](RemoveUserFromWorkspaceRequest.md) |  |  |

### Return type

**Object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_workspace

> Object update_workspace(workspace_uuid, workspace_input)

Update workspace

Updates a workspace's name, color, or access status. Admin only.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::WorkspacesApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
workspace_input = PostBoost::WorkspaceInput.new({name: 'name_example', hex_color: '#1d4ed8', access_status: 'subscription'}) # WorkspaceInput | 

begin
  # Update workspace
  result = api_instance.update_workspace(workspace_uuid, workspace_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling WorkspacesApi->update_workspace: #{e}"
end
```

#### Using the update_workspace_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> update_workspace_with_http_info(workspace_uuid, workspace_input)

```ruby
begin
  # Update workspace
  data, status_code, headers = api_instance.update_workspace_with_http_info(workspace_uuid, workspace_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue PostBoost::ApiError => e
  puts "Error when calling WorkspacesApi->update_workspace_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **workspace_input** | [**WorkspaceInput**](WorkspaceInput.md) |  |  |

### Return type

**Object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_workspace_user

> Object update_workspace_user(workspace_uuid, workspace_user_input)

Update user role in workspace

Changes a user's role or permissions within the workspace. Admin only.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::WorkspacesApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
workspace_user_input = PostBoost::WorkspaceUserInput.new({user_id: 37, role: 'admin', can_approve: false, is_owner: false}) # WorkspaceUserInput | 

begin
  # Update user role in workspace
  result = api_instance.update_workspace_user(workspace_uuid, workspace_user_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling WorkspacesApi->update_workspace_user: #{e}"
end
```

#### Using the update_workspace_user_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> update_workspace_user_with_http_info(workspace_uuid, workspace_user_input)

```ruby
begin
  # Update user role in workspace
  data, status_code, headers = api_instance.update_workspace_user_with_http_info(workspace_uuid, workspace_user_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue PostBoost::ApiError => e
  puts "Error when calling WorkspacesApi->update_workspace_user_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **workspace_user_input** | [**WorkspaceUserInput**](WorkspaceUserInput.md) |  |  |

### Return type

**Object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

