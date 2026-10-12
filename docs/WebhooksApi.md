# PostBoost::WebhooksApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_webhook_subscription**](WebhooksApi.md#create_webhook_subscription) | **POST** /{workspaceUuid}/webhooks/subscriptions | Subscribe a webhook |
| [**delete_webhook_subscription**](WebhooksApi.md#delete_webhook_subscription) | **DELETE** /{workspaceUuid}/webhooks/subscriptions/{subscriptionUuid} | Unsubscribe a webhook |
| [**list_webhook_subscriptions**](WebhooksApi.md#list_webhook_subscriptions) | **GET** /{workspaceUuid}/webhooks/subscriptions | List webhook subscriptions |


## create_webhook_subscription

> <CreateWebhookSubscription201Response> create_webhook_subscription(workspace_uuid, webhook_subscription_input)

Subscribe a webhook

Registers a callback URL for the given events, the way n8n, Zapier and Make instant triggers do. Deliveries are `POST` requests with a JSON body (see [Webhooks](/webhooks) for the payload), signed with the returned `secret` in `X-Signature` (HMAC-SHA256 of the raw body, hex encoded) and attempted up to 3 times. Only public `https://` URLs are accepted. The `secret` is in this response only. Workspace admins only. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::WebhooksApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
webhook_subscription_input = PostBoost::WebhookSubscriptionInput.new({callback_url: 'callback_url_example', events: [PostBoost::WebhookEventName::POST_SCHEDULED]}) # WebhookSubscriptionInput | 

begin
  # Subscribe a webhook
  result = api_instance.create_webhook_subscription(workspace_uuid, webhook_subscription_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling WebhooksApi->create_webhook_subscription: #{e}"
end
```

#### Using the create_webhook_subscription_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateWebhookSubscription201Response>, Integer, Hash)> create_webhook_subscription_with_http_info(workspace_uuid, webhook_subscription_input)

```ruby
begin
  # Subscribe a webhook
  data, status_code, headers = api_instance.create_webhook_subscription_with_http_info(workspace_uuid, webhook_subscription_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateWebhookSubscription201Response>
rescue PostBoost::ApiError => e
  puts "Error when calling WebhooksApi->create_webhook_subscription_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **webhook_subscription_input** | [**WebhookSubscriptionInput**](WebhookSubscriptionInput.md) |  |  |

### Return type

[**CreateWebhookSubscription201Response**](CreateWebhookSubscription201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_webhook_subscription

> Object delete_webhook_subscription(workspace_uuid, subscription_uuid)

Unsubscribe a webhook

Deletes the webhook and stops its deliveries. Workspace admins only.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::WebhooksApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
subscription_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the webhook subscription.

begin
  # Unsubscribe a webhook
  result = api_instance.delete_webhook_subscription(workspace_uuid, subscription_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling WebhooksApi->delete_webhook_subscription: #{e}"
end
```

#### Using the delete_webhook_subscription_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> delete_webhook_subscription_with_http_info(workspace_uuid, subscription_uuid)

```ruby
begin
  # Unsubscribe a webhook
  data, status_code, headers = api_instance.delete_webhook_subscription_with_http_info(workspace_uuid, subscription_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue PostBoost::ApiError => e
  puts "Error when calling WebhooksApi->delete_webhook_subscription_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **subscription_uuid** | **String** | UUID of the webhook subscription. |  |

### Return type

**Object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_webhook_subscriptions

> <ListWebhookSubscriptions200Response> list_webhook_subscriptions(workspace_uuid)

List webhook subscriptions

The workspace's webhooks, newest first: subscriptions created through this API and the ones added in **Settings → Webhooks**. Secrets are never returned here. Workspace admins only; needs the `webhooks` plan capability and, for scoped keys, the `webhooks` ability. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::WebhooksApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.

begin
  # List webhook subscriptions
  result = api_instance.list_webhook_subscriptions(workspace_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling WebhooksApi->list_webhook_subscriptions: #{e}"
end
```

#### Using the list_webhook_subscriptions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListWebhookSubscriptions200Response>, Integer, Hash)> list_webhook_subscriptions_with_http_info(workspace_uuid)

```ruby
begin
  # List webhook subscriptions
  data, status_code, headers = api_instance.list_webhook_subscriptions_with_http_info(workspace_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListWebhookSubscriptions200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling WebhooksApi->list_webhook_subscriptions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |

### Return type

[**ListWebhookSubscriptions200Response**](ListWebhookSubscriptions200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

