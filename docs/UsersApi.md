# PostBoost::UsersApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_user**](UsersApi.md#create_user) | **POST** /panel/users | Create user |
| [**delete_user**](UsersApi.md#delete_user) | **DELETE** /panel/users/{userId} | Delete user |
| [**delete_users_bulk**](UsersApi.md#delete_users_bulk) | **DELETE** /panel/users | Delete users (bulk) |
| [**get_user**](UsersApi.md#get_user) | **GET** /panel/users/{userId} | Get user |
| [**list_users**](UsersApi.md#list_users) | **GET** /panel/users | List users |
| [**update_user**](UsersApi.md#update_user) | **PUT** /panel/users/{userId} | Update user |


## create_user

> <User> create_user(user_input)

Create user

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::UsersApi.new
user_input = PostBoost::UserInput.new({name: 'name_example', email: 'email_example', password: 'password_example', password_confirmation: 'password_confirmation_example', is_admin: false}) # UserInput | 

begin
  # Create user
  result = api_instance.create_user(user_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling UsersApi->create_user: #{e}"
end
```

#### Using the create_user_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<User>, Integer, Hash)> create_user_with_http_info(user_input)

```ruby
begin
  # Create user
  data, status_code, headers = api_instance.create_user_with_http_info(user_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <User>
rescue PostBoost::ApiError => e
  puts "Error when calling UsersApi->create_user_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **user_input** | [**UserInput**](UserInput.md) |  |  |

### Return type

[**User**](User.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_user

> Object delete_user(user_id)

Delete user

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::UsersApi.new
user_id = 56 # Integer | ID of the user.

begin
  # Delete user
  result = api_instance.delete_user(user_id)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling UsersApi->delete_user: #{e}"
end
```

#### Using the delete_user_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> delete_user_with_http_info(user_id)

```ruby
begin
  # Delete user
  data, status_code, headers = api_instance.delete_user_with_http_info(user_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue PostBoost::ApiError => e
  puts "Error when calling UsersApi->delete_user_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **user_id** | **Integer** | ID of the user. |  |

### Return type

**Object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## delete_users_bulk

> Object delete_users_bulk(delete_users_bulk_request)

Delete users (bulk)

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::UsersApi.new
delete_users_bulk_request = PostBoost::DeleteUsersBulkRequest.new({users: [37]}) # DeleteUsersBulkRequest | 

begin
  # Delete users (bulk)
  result = api_instance.delete_users_bulk(delete_users_bulk_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling UsersApi->delete_users_bulk: #{e}"
end
```

#### Using the delete_users_bulk_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> delete_users_bulk_with_http_info(delete_users_bulk_request)

```ruby
begin
  # Delete users (bulk)
  data, status_code, headers = api_instance.delete_users_bulk_with_http_info(delete_users_bulk_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue PostBoost::ApiError => e
  puts "Error when calling UsersApi->delete_users_bulk_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **delete_users_bulk_request** | [**DeleteUsersBulkRequest**](DeleteUsersBulkRequest.md) |  |  |

### Return type

**Object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## get_user

> <User> get_user(user_id)

Get user

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::UsersApi.new
user_id = 56 # Integer | ID of the user.

begin
  # Get user
  result = api_instance.get_user(user_id)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling UsersApi->get_user: #{e}"
end
```

#### Using the get_user_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<User>, Integer, Hash)> get_user_with_http_info(user_id)

```ruby
begin
  # Get user
  data, status_code, headers = api_instance.get_user_with_http_info(user_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <User>
rescue PostBoost::ApiError => e
  puts "Error when calling UsersApi->get_user_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **user_id** | **Integer** | ID of the user. |  |

### Return type

[**User**](User.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_users

> <ListUsers200Response> list_users(opts)

List users

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::UsersApi.new
opts = {
  keyword: 'keyword_example' # String | Search by name or email.
}

begin
  # List users
  result = api_instance.list_users(opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling UsersApi->list_users: #{e}"
end
```

#### Using the list_users_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListUsers200Response>, Integer, Hash)> list_users_with_http_info(opts)

```ruby
begin
  # List users
  data, status_code, headers = api_instance.list_users_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListUsers200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling UsersApi->list_users_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **keyword** | **String** | Search by name or email. | [optional] |

### Return type

[**ListUsers200Response**](ListUsers200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_user

> Object update_user(user_id, user_update_input)

Update user

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::UsersApi.new
user_id = 56 # Integer | ID of the user.
user_update_input = PostBoost::UserUpdateInput.new({name: 'name_example', email: 'email_example', is_admin: false}) # UserUpdateInput | 

begin
  # Update user
  result = api_instance.update_user(user_id, user_update_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling UsersApi->update_user: #{e}"
end
```

#### Using the update_user_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> update_user_with_http_info(user_id, user_update_input)

```ruby
begin
  # Update user
  data, status_code, headers = api_instance.update_user_with_http_info(user_id, user_update_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue PostBoost::ApiError => e
  puts "Error when calling UsersApi->update_user_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **user_id** | **Integer** | ID of the user. |  |
| **user_update_input** | [**UserUpdateInput**](UserUpdateInput.md) |  |  |

### Return type

**Object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

