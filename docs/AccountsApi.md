# PostBoost::AccountsApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**connect_channel**](AccountsApi.md#connect_channel) | **POST** /{workspaceUuid}/accounts/connect/{provider} | Connect a Telegram, Discord or Slack channel |
| [**create_reconnect_link**](AccountsApi.md#create_reconnect_link) | **POST** /{workspaceUuid}/accounts/{accountUuid}/reconnect-links | Create a reconnect link |
| [**get_account**](AccountsApi.md#get_account) | **GET** /{workspaceUuid}/accounts/{accountUuid} | Get account |
| [**get_account_health**](AccountsApi.md#get_account_health) | **GET** /{workspaceUuid}/account-health | Account health |
| [**list_accounts**](AccountsApi.md#list_accounts) | **GET** /{workspaceUuid}/accounts | List accounts |


## connect_channel

> <ChannelAccount> connect_channel(workspace_uuid, provider, connect_channel_input)

Connect a Telegram, Discord or Slack channel

Connects a channel that uses a bot token or a webhook URL instead of a login. The credentials are checked against the network first, stored encrypted and never returned. Connecting the same channel again updates it (`200`) instead of adding a second account. Workspace admins only; counts toward the plan's social account limit.  - **telegram**: `bot_token` from @BotFather and `chat` (the channel's `@username`, or its   numeric id such as `-1001234567890` for a private channel). The bot must be an administrator   of the channel allowed to post messages. - **discord**: `webhook_url` from Channel settings → Integrations → Webhooks   (`https://discord.com/api/webhooks/…`). - **slack**: `webhook_url` of an incoming webhook (`https://hooks.slack.com/services/…`) and an   optional display `name`. Slack posts cannot be deleted from PostBoost, and images must be   publicly reachable.  Webhook URLs on any other host are refused (`422`) before any request is made. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::AccountsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
provider = 'telegram' # String | 
connect_channel_input = PostBoost::ConnectChannelInput.new # ConnectChannelInput | 

begin
  # Connect a Telegram, Discord or Slack channel
  result = api_instance.connect_channel(workspace_uuid, provider, connect_channel_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AccountsApi->connect_channel: #{e}"
end
```

#### Using the connect_channel_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ChannelAccount>, Integer, Hash)> connect_channel_with_http_info(workspace_uuid, provider, connect_channel_input)

```ruby
begin
  # Connect a Telegram, Discord or Slack channel
  data, status_code, headers = api_instance.connect_channel_with_http_info(workspace_uuid, provider, connect_channel_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ChannelAccount>
rescue PostBoost::ApiError => e
  puts "Error when calling AccountsApi->connect_channel_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **provider** | **String** |  |  |
| **connect_channel_input** | [**ConnectChannelInput**](ConnectChannelInput.md) |  |  |

### Return type

[**ChannelAccount**](ChannelAccount.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## create_reconnect_link

> <ReconnectLink> create_reconnect_link(workspace_uuid, account_uuid)

Create a reconnect link

Creates a single-use link (valid 7 days) that lets someone without a PostBoost login, such as an agency's client, re-authorize this one account on its network. The link only refreshes the connection of this account; signing in as a different profile or page changes nothing. Workspace admins only. Available for Facebook Pages, Instagram, Threads, LinkedIn, TikTok, YouTube and Pinterest. Returns `404` while the feature is not enabled on this instance. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::AccountsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
account_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the social media account.

begin
  # Create a reconnect link
  result = api_instance.create_reconnect_link(workspace_uuid, account_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AccountsApi->create_reconnect_link: #{e}"
end
```

#### Using the create_reconnect_link_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ReconnectLink>, Integer, Hash)> create_reconnect_link_with_http_info(workspace_uuid, account_uuid)

```ruby
begin
  # Create a reconnect link
  data, status_code, headers = api_instance.create_reconnect_link_with_http_info(workspace_uuid, account_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ReconnectLink>
rescue PostBoost::ApiError => e
  puts "Error when calling AccountsApi->create_reconnect_link_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **account_uuid** | **String** | UUID of the social media account. |  |

### Return type

[**ReconnectLink**](ReconnectLink.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_account

> <Account> get_account(workspace_uuid, account_uuid)

Get account

Returns a single social media account.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::AccountsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
account_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the social media account.

begin
  # Get account
  result = api_instance.get_account(workspace_uuid, account_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AccountsApi->get_account: #{e}"
end
```

#### Using the get_account_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Account>, Integer, Hash)> get_account_with_http_info(workspace_uuid, account_uuid)

```ruby
begin
  # Get account
  data, status_code, headers = api_instance.get_account_with_http_info(workspace_uuid, account_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Account>
rescue PostBoost::ApiError => e
  puts "Error when calling AccountsApi->get_account_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **account_uuid** | **String** | UUID of the social media account. |  |

### Return type

[**Account**](Account.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_account_health

> <GetAccountHealth200Response> get_account_health(workspace_uuid)

Account health

Pre-flight health of every account in the workspace: whether it is authorized and holds an access token, how much of its daily post cap (per UTC day, scheduled, awaiting approval and published posts) is used today, and its connection health: predicted token expiry, latest publish outcome and where to reconnect it. The `account.token_expiring` and `account.disconnected` webhooks report changes as they happen. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::AccountsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.

begin
  # Account health
  result = api_instance.get_account_health(workspace_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AccountsApi->get_account_health: #{e}"
end
```

#### Using the get_account_health_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetAccountHealth200Response>, Integer, Hash)> get_account_health_with_http_info(workspace_uuid)

```ruby
begin
  # Account health
  data, status_code, headers = api_instance.get_account_health_with_http_info(workspace_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetAccountHealth200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling AccountsApi->get_account_health_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |

### Return type

[**GetAccountHealth200Response**](GetAccountHealth200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_accounts

> <ListAccounts200Response> list_accounts(workspace_uuid, opts)

List accounts

Returns all social media accounts connected to the workspace, newest first. Optional filters narrow the list.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::AccountsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
opts = {
  keyword: 'keyword_example', # String | Match the account name or username.
  group: 'group_example', # String | Only accounts in this account group.
  providers: ['inner_example'], # Array<String> | Only accounts of these providers (for example `instagram`, `linkedin`).
  unauthorized: true # Boolean | When `true`, only accounts that need to be reconnected.
}

begin
  # List accounts
  result = api_instance.list_accounts(workspace_uuid, opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AccountsApi->list_accounts: #{e}"
end
```

#### Using the list_accounts_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListAccounts200Response>, Integer, Hash)> list_accounts_with_http_info(workspace_uuid, opts)

```ruby
begin
  # List accounts
  data, status_code, headers = api_instance.list_accounts_with_http_info(workspace_uuid, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListAccounts200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling AccountsApi->list_accounts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **keyword** | **String** | Match the account name or username. | [optional] |
| **group** | **String** | Only accounts in this account group. | [optional] |
| **providers** | [**Array&lt;String&gt;**](String.md) | Only accounts of these providers (for example &#x60;instagram&#x60;, &#x60;linkedin&#x60;). | [optional] |
| **unauthorized** | **Boolean** | When &#x60;true&#x60;, only accounts that need to be reconnected. | [optional] |

### Return type

[**ListAccounts200Response**](ListAccounts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

