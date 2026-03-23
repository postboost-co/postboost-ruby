# PostBoost::AccountsApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_account**](AccountsApi.md#get_account) | **GET** /{workspaceUuid}/accounts/{accountUuid} | Get account |
| [**list_accounts**](AccountsApi.md#list_accounts) | **GET** /{workspaceUuid}/accounts | List accounts |


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


## list_accounts

> <ListAccounts200Response> list_accounts(workspace_uuid)

List accounts

Returns all social media accounts connected to the workspace.

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
  # List accounts
  result = api_instance.list_accounts(workspace_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AccountsApi->list_accounts: #{e}"
end
```

#### Using the list_accounts_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListAccounts200Response>, Integer, Hash)> list_accounts_with_http_info(workspace_uuid)

```ruby
begin
  # List accounts
  data, status_code, headers = api_instance.list_accounts_with_http_info(workspace_uuid)
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

### Return type

[**ListAccounts200Response**](ListAccounts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

