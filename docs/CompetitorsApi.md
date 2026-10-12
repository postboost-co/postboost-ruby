# PostBoost::CompetitorsApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**add_competitor**](CompetitorsApi.md#add_competitor) | **POST** /{workspaceUuid}/competitors | Track a competitor |
| [**delete_competitor**](CompetitorsApi.md#delete_competitor) | **DELETE** /{workspaceUuid}/competitors/{competitorId} | Stop tracking a competitor |
| [**get_competitor**](CompetitorsApi.md#get_competitor) | **GET** /{workspaceUuid}/competitors/{competitorId} | Get a competitor |
| [**list_competitors**](CompetitorsApi.md#list_competitors) | **GET** /{workspaceUuid}/competitors | List competitors |


## add_competitor

> <AddCompetitor202Response> add_competitor(workspace_uuid, competitor_input)

Track a competitor

Starts tracking a public Instagram business or creator account from one of your Instagram accounts (connected through a Facebook Page). Returns `202` at once; followers, snapshots and recent media appear after the background import. `409` if that account already tracks the username. Admins and members only (not viewers). 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::CompetitorsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
competitor_input = PostBoost::CompetitorInput.new({account_id: 37, username: 'natgeo'}) # CompetitorInput | 

begin
  # Track a competitor
  result = api_instance.add_competitor(workspace_uuid, competitor_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling CompetitorsApi->add_competitor: #{e}"
end
```

#### Using the add_competitor_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AddCompetitor202Response>, Integer, Hash)> add_competitor_with_http_info(workspace_uuid, competitor_input)

```ruby
begin
  # Track a competitor
  data, status_code, headers = api_instance.add_competitor_with_http_info(workspace_uuid, competitor_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AddCompetitor202Response>
rescue PostBoost::ApiError => e
  puts "Error when calling CompetitorsApi->add_competitor_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **competitor_input** | [**CompetitorInput**](CompetitorInput.md) |  |  |

### Return type

[**AddCompetitor202Response**](AddCompetitor202Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_competitor

> delete_competitor(workspace_uuid, competitor_id)

Stop tracking a competitor

Deletes the competitor with its snapshots and media. Admins and members only (not viewers). 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::CompetitorsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
competitor_id = 56 # Integer | The competitor `id`.

begin
  # Stop tracking a competitor
  api_instance.delete_competitor(workspace_uuid, competitor_id)
rescue PostBoost::ApiError => e
  puts "Error when calling CompetitorsApi->delete_competitor: #{e}"
end
```

#### Using the delete_competitor_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_competitor_with_http_info(workspace_uuid, competitor_id)

```ruby
begin
  # Stop tracking a competitor
  data, status_code, headers = api_instance.delete_competitor_with_http_info(workspace_uuid, competitor_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue PostBoost::ApiError => e
  puts "Error when calling CompetitorsApi->delete_competitor_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **competitor_id** | **Integer** | The competitor &#x60;id&#x60;. |  |

### Return type

nil (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_competitor

> <GetCompetitor200Response> get_competitor(workspace_uuid, competitor_id)

Get a competitor

The competitor with daily follower snapshots for the last 90 days and its 12 most recent posts. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::CompetitorsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
competitor_id = 56 # Integer | The competitor `id`.

begin
  # Get a competitor
  result = api_instance.get_competitor(workspace_uuid, competitor_id)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling CompetitorsApi->get_competitor: #{e}"
end
```

#### Using the get_competitor_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetCompetitor200Response>, Integer, Hash)> get_competitor_with_http_info(workspace_uuid, competitor_id)

```ruby
begin
  # Get a competitor
  data, status_code, headers = api_instance.get_competitor_with_http_info(workspace_uuid, competitor_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetCompetitor200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling CompetitorsApi->get_competitor_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **competitor_id** | **Integer** | The competitor &#x60;id&#x60;. |  |

### Return type

[**GetCompetitor200Response**](GetCompetitor200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_competitors

> <ListCompetitors200Response> list_competitors(workspace_uuid, opts)

List competitors

Instagram business or creator accounts the workspace tracks, by follower count. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::CompetitorsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
opts = {
  account_id: 56 # Integer | Only competitors tracked from this Instagram account `id`.
}

begin
  # List competitors
  result = api_instance.list_competitors(workspace_uuid, opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling CompetitorsApi->list_competitors: #{e}"
end
```

#### Using the list_competitors_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListCompetitors200Response>, Integer, Hash)> list_competitors_with_http_info(workspace_uuid, opts)

```ruby
begin
  # List competitors
  data, status_code, headers = api_instance.list_competitors_with_http_info(workspace_uuid, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListCompetitors200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling CompetitorsApi->list_competitors_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **account_id** | **Integer** | Only competitors tracked from this Instagram account &#x60;id&#x60;. | [optional] |

### Return type

[**ListCompetitors200Response**](ListCompetitors200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

