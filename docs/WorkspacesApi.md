# PostBoost::WorkspacesApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**add_user_to_workspace**](WorkspacesApi.md#add_user_to_workspace) | **POST** /panel/workspaces/{workspaceUuid}/users | Add user to workspace |
| [**create_api_key**](WorkspacesApi.md#create_api_key) | **POST** /{workspaceUuid}/api-keys | Create a scoped API key |
| [**create_reseller_client**](WorkspacesApi.md#create_reseller_client) | **POST** /{workspaceUuid}/clients | Create a client workspace |
| [**create_workspace**](WorkspacesApi.md#create_workspace) | **POST** /panel/workspaces | Create workspace |
| [**delete_api_key**](WorkspacesApi.md#delete_api_key) | **DELETE** /{workspaceUuid}/api-keys/{apiKeyId} | Revoke a scoped API key |
| [**delete_workspace**](WorkspacesApi.md#delete_workspace) | **DELETE** /panel/workspaces/{workspaceUuid} | Delete workspace |
| [**delete_workspaces_bulk**](WorkspacesApi.md#delete_workspaces_bulk) | **DELETE** /panel/workspaces | Delete workspaces (bulk) |
| [**get_workspace**](WorkspacesApi.md#get_workspace) | **GET** /panel/workspaces/{workspaceUuid} | Get workspace |
| [**get_workspace_ai_credits**](WorkspacesApi.md#get_workspace_ai_credits) | **GET** /panel/workspaces/{workspaceUuid}/ai-credits | Get workspace AI credits |
| [**get_x_usage**](WorkspacesApi.md#get_x_usage) | **GET** /{workspaceUuid}/usage/x | X (Twitter) usage |
| [**list_api_keys**](WorkspacesApi.md#list_api_keys) | **GET** /{workspaceUuid}/api-keys | List scoped API keys |
| [**list_my_workspaces**](WorkspacesApi.md#list_my_workspaces) | **GET** /workspaces | List my workspaces |
| [**list_reseller_clients**](WorkspacesApi.md#list_reseller_clients) | **GET** /{workspaceUuid}/clients | List client workspaces |
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


## create_api_key

> <CreateApiKey201Response> create_api_key(workspace_uuid, api_key_input)

Create a scoped API key

Creates a least-privilege API key for the calling user, bound to this workspace. Pick the abilities it gets and, optionally, the accounts it may act on. The plain key is in `data.token` of this response only; store it safely.  | Ability | Allows | |---|---| | `read` | Every `GET`, plus the `posts/validate` dry run | | `write` | Creating and changing drafts, media, tags, mentions, the brand voice | | `publish` | Scheduling, queueing, publishing now, approving and retrying posts, and editing a post that is already scheduled | | `ai` | The `/ai/*` endpoints, running agents and turning on agent AI review (they also need AI credits) | | `webhooks` | Webhook subscription endpoints |  A scoped key is refused on other workspaces, on the admin panel, on API key management and on the app's built-in MCP endpoint (use `/mcp/postboost`). With `account_ids`, it may only name those accounts (in the URL, `accounts`, `account_ids` or post versions), cannot touch posts on other accounts, and `GET accounts` / `GET posts` only list matching items (pagination counts are computed before that filter). Workspace admins only, called with an unscoped key. 

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
api_key_input = PostBoost::ApiKeyInput.new({name: 'name_example', abilities: [PostBoost::ApiKeyAbility::READ]}) # ApiKeyInput | 

begin
  # Create a scoped API key
  result = api_instance.create_api_key(workspace_uuid, api_key_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling WorkspacesApi->create_api_key: #{e}"
end
```

#### Using the create_api_key_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateApiKey201Response>, Integer, Hash)> create_api_key_with_http_info(workspace_uuid, api_key_input)

```ruby
begin
  # Create a scoped API key
  data, status_code, headers = api_instance.create_api_key_with_http_info(workspace_uuid, api_key_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateApiKey201Response>
rescue PostBoost::ApiError => e
  puts "Error when calling WorkspacesApi->create_api_key_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **api_key_input** | [**ApiKeyInput**](ApiKeyInput.md) |  |  |

### Return type

[**CreateApiKey201Response**](CreateApiKey201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## create_reseller_client

> <CreateResellerClient201Response> create_reseller_client(workspace_uuid, reseller_client_input)

Create a client workspace

Creates a client workspace on the Reseller client plan, with the caller as its owner and admin, and links it to this workspace. Fails with `422` and `code: client_limit_reached` once the plan's client limit is used (archived clients do not count). Archive clients on the Client workspaces page. Workspace admins with an unscoped key only. 

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
reseller_client_input = PostBoost::ResellerClientInput.new({name: 'name_example'}) # ResellerClientInput | 

begin
  # Create a client workspace
  result = api_instance.create_reseller_client(workspace_uuid, reseller_client_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling WorkspacesApi->create_reseller_client: #{e}"
end
```

#### Using the create_reseller_client_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateResellerClient201Response>, Integer, Hash)> create_reseller_client_with_http_info(workspace_uuid, reseller_client_input)

```ruby
begin
  # Create a client workspace
  data, status_code, headers = api_instance.create_reseller_client_with_http_info(workspace_uuid, reseller_client_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateResellerClient201Response>
rescue PostBoost::ApiError => e
  puts "Error when calling WorkspacesApi->create_reseller_client_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **reseller_client_input** | [**ResellerClientInput**](ResellerClientInput.md) |  |  |

### Return type

[**CreateResellerClient201Response**](CreateResellerClient201Response.md)

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
workspace_input = PostBoost::WorkspaceInput.new({name: 'name_example', access_status: 'subscription'}) # WorkspaceInput | 

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


## delete_api_key

> Object delete_api_key(workspace_uuid, api_key_id)

Revoke a scoped API key

Revokes a scoped key bound to this workspace. It stops working at once. Workspace admins only, called with an unscoped key.

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
api_key_id = 56 # Integer | The key's `id` from `GET api-keys`.

begin
  # Revoke a scoped API key
  result = api_instance.delete_api_key(workspace_uuid, api_key_id)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling WorkspacesApi->delete_api_key: #{e}"
end
```

#### Using the delete_api_key_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> delete_api_key_with_http_info(workspace_uuid, api_key_id)

```ruby
begin
  # Revoke a scoped API key
  data, status_code, headers = api_instance.delete_api_key_with_http_info(workspace_uuid, api_key_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue PostBoost::ApiError => e
  puts "Error when calling WorkspacesApi->delete_api_key_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **api_key_id** | **Integer** | The key&#39;s &#x60;id&#x60; from &#x60;GET api-keys&#x60;. |  |

### Return type

**Object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
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


## get_workspace_ai_credits

> <AICredits> get_workspace_ai_credits(workspace_uuid)

Get workspace AI credits

Returns whether the workspace can use AI credits, its remaining balance, and whether the balance is low. Admin only.

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
  # Get workspace AI credits
  result = api_instance.get_workspace_ai_credits(workspace_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling WorkspacesApi->get_workspace_ai_credits: #{e}"
end
```

#### Using the get_workspace_ai_credits_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AICredits>, Integer, Hash)> get_workspace_ai_credits_with_http_info(workspace_uuid)

```ruby
begin
  # Get workspace AI credits
  data, status_code, headers = api_instance.get_workspace_ai_credits_with_http_info(workspace_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AICredits>
rescue PostBoost::ApiError => e
  puts "Error when calling WorkspacesApi->get_workspace_ai_credits_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |

### Return type

[**AICredits**](AICredits.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_x_usage

> <XUsage> get_x_usage(workspace_uuid)

X (Twitter) usage

The workspace's X posts this calendar month (UTC) against its monthly X allowance. Every thread part is one X post; a part with a link also counts as a link post. When the allowance is used up, scheduling to X is refused (`429`, `code: x_monthly_cap_reached`) and X posts that come due fail with \"Monthly X allowance reached\". Other networks are not affected. See the X policy in the developer docs. 

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
  # X (Twitter) usage
  result = api_instance.get_x_usage(workspace_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling WorkspacesApi->get_x_usage: #{e}"
end
```

#### Using the get_x_usage_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<XUsage>, Integer, Hash)> get_x_usage_with_http_info(workspace_uuid)

```ruby
begin
  # X (Twitter) usage
  data, status_code, headers = api_instance.get_x_usage_with_http_info(workspace_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <XUsage>
rescue PostBoost::ApiError => e
  puts "Error when calling WorkspacesApi->get_x_usage_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |

### Return type

[**XUsage**](XUsage.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_api_keys

> <ListApiKeys200Response> list_api_keys(workspace_uuid)

List scoped API keys

Scoped API keys bound to this workspace, newest first. The secret is never shown again after creation. Workspace admins only, called with an unscoped key (a scoped key gets `403` with `code: insufficient_scope`). 

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
  # List scoped API keys
  result = api_instance.list_api_keys(workspace_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling WorkspacesApi->list_api_keys: #{e}"
end
```

#### Using the list_api_keys_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListApiKeys200Response>, Integer, Hash)> list_api_keys_with_http_info(workspace_uuid)

```ruby
begin
  # List scoped API keys
  data, status_code, headers = api_instance.list_api_keys_with_http_info(workspace_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListApiKeys200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling WorkspacesApi->list_api_keys_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |

### Return type

[**ListApiKeys200Response**](ListApiKeys200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_my_workspaces

> <ListMyWorkspaces200Response> list_my_workspaces

List my workspaces

Returns the workspaces the authenticated user belongs to, most recently updated first, with the caller's role in each. Use a returned `uuid` as `workspaceUuid`.

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

begin
  # List my workspaces
  result = api_instance.list_my_workspaces
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling WorkspacesApi->list_my_workspaces: #{e}"
end
```

#### Using the list_my_workspaces_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListMyWorkspaces200Response>, Integer, Hash)> list_my_workspaces_with_http_info

```ruby
begin
  # List my workspaces
  data, status_code, headers = api_instance.list_my_workspaces_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListMyWorkspaces200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling WorkspacesApi->list_my_workspaces_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**ListMyWorkspaces200Response**](ListMyWorkspaces200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_reseller_clients

> <ListResellerClients200Response> list_reseller_clients(workspace_uuid)

List client workspaces

Client workspaces this workspace created on the Reseller plan, active first, then archived. `accounts_needing_reconnect` counts accounts whose connection must be renewed. `meta` gives the active clients and the plan's client limit. Workspace admins with an unscoped key only; other workspaces get `403` with `code: not_a_reseller`. 

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
  # List client workspaces
  result = api_instance.list_reseller_clients(workspace_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling WorkspacesApi->list_reseller_clients: #{e}"
end
```

#### Using the list_reseller_clients_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListResellerClients200Response>, Integer, Hash)> list_reseller_clients_with_http_info(workspace_uuid)

```ruby
begin
  # List client workspaces
  data, status_code, headers = api_instance.list_reseller_clients_with_http_info(workspace_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListResellerClients200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling WorkspacesApi->list_reseller_clients_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |

### Return type

[**ListResellerClients200Response**](ListResellerClients200Response.md)

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

Updates a workspace's name, owner, or access status. Admin only. `hex_color` is accepted but ignored.

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
workspace_input = PostBoost::WorkspaceInput.new({name: 'name_example', access_status: 'subscription'}) # WorkspaceInput | 

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

