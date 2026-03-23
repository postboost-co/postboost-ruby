# PostBoost::SubscriptionsApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**add_generic_subscription**](SubscriptionsApi.md#add_generic_subscription) | **POST** /panel/workspaces/{workspaceUuid}/subscription/generic | Add generic subscription |
| [**cancel_subscription**](SubscriptionsApi.md#cancel_subscription) | **POST** /panel/workspaces/{workspaceUuid}/subscription/cancel | Cancel subscription |
| [**change_subscription_plan**](SubscriptionsApi.md#change_subscription_plan) | **PUT** /panel/workspaces/{workspaceUuid}/subscription/change-plan | Change subscription plan |
| [**checkout_subscription**](SubscriptionsApi.md#checkout_subscription) | **POST** /panel/workspaces/{workspaceUuid}/subscription/new | New subscription checkout |
| [**create_subscription**](SubscriptionsApi.md#create_subscription) | **POST** /panel/workspaces/{workspaceUuid}/subscription | Create subscription |
| [**delete_subscription**](SubscriptionsApi.md#delete_subscription) | **DELETE** /panel/workspaces/{workspaceUuid}/subscription | Delete subscription |
| [**get_subscription**](SubscriptionsApi.md#get_subscription) | **GET** /panel/workspaces/{workspaceUuid}/subscription | Get subscription |
| [**remove_generic_subscription**](SubscriptionsApi.md#remove_generic_subscription) | **DELETE** /panel/workspaces/{workspaceUuid}/subscription/generic | Remove generic subscription |
| [**resume_subscription**](SubscriptionsApi.md#resume_subscription) | **POST** /panel/workspaces/{workspaceUuid}/subscription/resume | Resume subscription |
| [**update_subscription**](SubscriptionsApi.md#update_subscription) | **PUT** /panel/workspaces/{workspaceUuid}/subscription | Update subscription |


## add_generic_subscription

> Object add_generic_subscription(workspace_uuid, add_generic_subscription_request)

Add generic subscription

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::SubscriptionsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
add_generic_subscription_request = PostBoost::AddGenericSubscriptionRequest.new({plan_id: 37, keep_prev_trial_ends_at: false}) # AddGenericSubscriptionRequest | 

begin
  # Add generic subscription
  result = api_instance.add_generic_subscription(workspace_uuid, add_generic_subscription_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling SubscriptionsApi->add_generic_subscription: #{e}"
end
```

#### Using the add_generic_subscription_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> add_generic_subscription_with_http_info(workspace_uuid, add_generic_subscription_request)

```ruby
begin
  # Add generic subscription
  data, status_code, headers = api_instance.add_generic_subscription_with_http_info(workspace_uuid, add_generic_subscription_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue PostBoost::ApiError => e
  puts "Error when calling SubscriptionsApi->add_generic_subscription_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **add_generic_subscription_request** | [**AddGenericSubscriptionRequest**](AddGenericSubscriptionRequest.md) |  |  |

### Return type

**Object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## cancel_subscription

> Object cancel_subscription(workspace_uuid)

Cancel subscription

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::SubscriptionsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.

begin
  # Cancel subscription
  result = api_instance.cancel_subscription(workspace_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling SubscriptionsApi->cancel_subscription: #{e}"
end
```

#### Using the cancel_subscription_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> cancel_subscription_with_http_info(workspace_uuid)

```ruby
begin
  # Cancel subscription
  data, status_code, headers = api_instance.cancel_subscription_with_http_info(workspace_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue PostBoost::ApiError => e
  puts "Error when calling SubscriptionsApi->cancel_subscription_with_http_info: #{e}"
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


## change_subscription_plan

> Object change_subscription_plan(workspace_uuid, change_subscription_plan_request)

Change subscription plan

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::SubscriptionsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
change_subscription_plan_request = PostBoost::ChangeSubscriptionPlanRequest.new({plan_id: 37, cycle: 'monthly', prorate: false, billing_immediately: false}) # ChangeSubscriptionPlanRequest | 

begin
  # Change subscription plan
  result = api_instance.change_subscription_plan(workspace_uuid, change_subscription_plan_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling SubscriptionsApi->change_subscription_plan: #{e}"
end
```

#### Using the change_subscription_plan_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> change_subscription_plan_with_http_info(workspace_uuid, change_subscription_plan_request)

```ruby
begin
  # Change subscription plan
  data, status_code, headers = api_instance.change_subscription_plan_with_http_info(workspace_uuid, change_subscription_plan_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue PostBoost::ApiError => e
  puts "Error when calling SubscriptionsApi->change_subscription_plan_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **change_subscription_plan_request** | [**ChangeSubscriptionPlanRequest**](ChangeSubscriptionPlanRequest.md) |  |  |

### Return type

**Object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## checkout_subscription

> <CheckoutSubscription200Response> checkout_subscription(workspace_uuid, checkout_subscription_request)

New subscription checkout

Returns a Stripe Checkout URL for a new subscription.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::SubscriptionsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
checkout_subscription_request = PostBoost::CheckoutSubscriptionRequest.new({plan_id: 37, cycle: 'monthly'}) # CheckoutSubscriptionRequest | 

begin
  # New subscription checkout
  result = api_instance.checkout_subscription(workspace_uuid, checkout_subscription_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling SubscriptionsApi->checkout_subscription: #{e}"
end
```

#### Using the checkout_subscription_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CheckoutSubscription200Response>, Integer, Hash)> checkout_subscription_with_http_info(workspace_uuid, checkout_subscription_request)

```ruby
begin
  # New subscription checkout
  data, status_code, headers = api_instance.checkout_subscription_with_http_info(workspace_uuid, checkout_subscription_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CheckoutSubscription200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling SubscriptionsApi->checkout_subscription_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **checkout_subscription_request** | [**CheckoutSubscriptionRequest**](CheckoutSubscriptionRequest.md) |  |  |

### Return type

[**CheckoutSubscription200Response**](CheckoutSubscription200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## create_subscription

> Object create_subscription(workspace_uuid, subscription_input)

Create subscription

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::SubscriptionsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
subscription_input = PostBoost::SubscriptionInput.new({platform_subscription_id: 'platform_subscription_id_example', platform_plan_id: 'platform_plan_id_example', status: PostBoost::SubscriptionStatus::ACTIVE}) # SubscriptionInput | 

begin
  # Create subscription
  result = api_instance.create_subscription(workspace_uuid, subscription_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling SubscriptionsApi->create_subscription: #{e}"
end
```

#### Using the create_subscription_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> create_subscription_with_http_info(workspace_uuid, subscription_input)

```ruby
begin
  # Create subscription
  data, status_code, headers = api_instance.create_subscription_with_http_info(workspace_uuid, subscription_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue PostBoost::ApiError => e
  puts "Error when calling SubscriptionsApi->create_subscription_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **subscription_input** | [**SubscriptionInput**](SubscriptionInput.md) |  |  |

### Return type

**Object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_subscription

> Object delete_subscription(workspace_uuid)

Delete subscription

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::SubscriptionsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.

begin
  # Delete subscription
  result = api_instance.delete_subscription(workspace_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling SubscriptionsApi->delete_subscription: #{e}"
end
```

#### Using the delete_subscription_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> delete_subscription_with_http_info(workspace_uuid)

```ruby
begin
  # Delete subscription
  data, status_code, headers = api_instance.delete_subscription_with_http_info(workspace_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue PostBoost::ApiError => e
  puts "Error when calling SubscriptionsApi->delete_subscription_with_http_info: #{e}"
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


## get_subscription

> <Subscription> get_subscription(workspace_uuid)

Get subscription

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::SubscriptionsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.

begin
  # Get subscription
  result = api_instance.get_subscription(workspace_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling SubscriptionsApi->get_subscription: #{e}"
end
```

#### Using the get_subscription_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Subscription>, Integer, Hash)> get_subscription_with_http_info(workspace_uuid)

```ruby
begin
  # Get subscription
  data, status_code, headers = api_instance.get_subscription_with_http_info(workspace_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Subscription>
rescue PostBoost::ApiError => e
  puts "Error when calling SubscriptionsApi->get_subscription_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |

### Return type

[**Subscription**](Subscription.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## remove_generic_subscription

> Object remove_generic_subscription(workspace_uuid)

Remove generic subscription

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::SubscriptionsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.

begin
  # Remove generic subscription
  result = api_instance.remove_generic_subscription(workspace_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling SubscriptionsApi->remove_generic_subscription: #{e}"
end
```

#### Using the remove_generic_subscription_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> remove_generic_subscription_with_http_info(workspace_uuid)

```ruby
begin
  # Remove generic subscription
  data, status_code, headers = api_instance.remove_generic_subscription_with_http_info(workspace_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue PostBoost::ApiError => e
  puts "Error when calling SubscriptionsApi->remove_generic_subscription_with_http_info: #{e}"
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


## resume_subscription

> Object resume_subscription(workspace_uuid)

Resume subscription

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::SubscriptionsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.

begin
  # Resume subscription
  result = api_instance.resume_subscription(workspace_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling SubscriptionsApi->resume_subscription: #{e}"
end
```

#### Using the resume_subscription_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> resume_subscription_with_http_info(workspace_uuid)

```ruby
begin
  # Resume subscription
  data, status_code, headers = api_instance.resume_subscription_with_http_info(workspace_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue PostBoost::ApiError => e
  puts "Error when calling SubscriptionsApi->resume_subscription_with_http_info: #{e}"
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


## update_subscription

> Object update_subscription(workspace_uuid, subscription_update_input)

Update subscription

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::SubscriptionsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
subscription_update_input = PostBoost::SubscriptionUpdateInput.new({platform_plan_id: 'platform_plan_id_example', status: PostBoost::SubscriptionStatus::ACTIVE}) # SubscriptionUpdateInput | 

begin
  # Update subscription
  result = api_instance.update_subscription(workspace_uuid, subscription_update_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling SubscriptionsApi->update_subscription: #{e}"
end
```

#### Using the update_subscription_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> update_subscription_with_http_info(workspace_uuid, subscription_update_input)

```ruby
begin
  # Update subscription
  data, status_code, headers = api_instance.update_subscription_with_http_info(workspace_uuid, subscription_update_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue PostBoost::ApiError => e
  puts "Error when calling SubscriptionsApi->update_subscription_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **subscription_update_input** | [**SubscriptionUpdateInput**](SubscriptionUpdateInput.md) |  |  |

### Return type

**Object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

