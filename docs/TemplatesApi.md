# PostBoost::TemplatesApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_template**](TemplatesApi.md#create_template) | **POST** /{workspaceUuid}/templates | Create a template |
| [**delete_template**](TemplatesApi.md#delete_template) | **DELETE** /{workspaceUuid}/templates/{templateId} | Delete a template |
| [**get_template**](TemplatesApi.md#get_template) | **GET** /{workspaceUuid}/templates/{templateId} | Get a template |
| [**list_templates**](TemplatesApi.md#list_templates) | **GET** /{workspaceUuid}/templates | List templates |
| [**update_template**](TemplatesApi.md#update_template) | **PUT** /{workspaceUuid}/templates/{templateId} | Update a template |


## create_template

> <CreateTemplate201Response> create_template(workspace_uuid, template_input)

Create a template

Creates a post template: a name and one or more content items (body plus media ids from the media library). Admins and members only (not viewers). 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::TemplatesApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
template_input = PostBoost::TemplateInput.new({name: 'name_example'}) # TemplateInput | 

begin
  # Create a template
  result = api_instance.create_template(workspace_uuid, template_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling TemplatesApi->create_template: #{e}"
end
```

#### Using the create_template_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateTemplate201Response>, Integer, Hash)> create_template_with_http_info(workspace_uuid, template_input)

```ruby
begin
  # Create a template
  data, status_code, headers = api_instance.create_template_with_http_info(workspace_uuid, template_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateTemplate201Response>
rescue PostBoost::ApiError => e
  puts "Error when calling TemplatesApi->create_template_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **template_input** | [**TemplateInput**](TemplateInput.md) |  |  |

### Return type

[**CreateTemplate201Response**](CreateTemplate201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_template

> delete_template(workspace_uuid, template_id)

Delete a template

Admins and members only (not viewers). 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::TemplatesApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
template_id = 'template_id_example' # String | The template `id`.

begin
  # Delete a template
  api_instance.delete_template(workspace_uuid, template_id)
rescue PostBoost::ApiError => e
  puts "Error when calling TemplatesApi->delete_template: #{e}"
end
```

#### Using the delete_template_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_template_with_http_info(workspace_uuid, template_id)

```ruby
begin
  # Delete a template
  data, status_code, headers = api_instance.delete_template_with_http_info(workspace_uuid, template_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue PostBoost::ApiError => e
  puts "Error when calling TemplatesApi->delete_template_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **template_id** | **String** | The template &#x60;id&#x60;. |  |

### Return type

nil (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_template

> <CreateTemplate201Response> get_template(workspace_uuid, template_id)

Get a template

One template. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::TemplatesApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
template_id = 'template_id_example' # String | The template `id`.

begin
  # Get a template
  result = api_instance.get_template(workspace_uuid, template_id)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling TemplatesApi->get_template: #{e}"
end
```

#### Using the get_template_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateTemplate201Response>, Integer, Hash)> get_template_with_http_info(workspace_uuid, template_id)

```ruby
begin
  # Get a template
  data, status_code, headers = api_instance.get_template_with_http_info(workspace_uuid, template_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateTemplate201Response>
rescue PostBoost::ApiError => e
  puts "Error when calling TemplatesApi->get_template_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **template_id** | **String** | The template &#x60;id&#x60;. |  |

### Return type

[**CreateTemplate201Response**](CreateTemplate201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_templates

> <ListTemplates200Response> list_templates(workspace_uuid, opts)

List templates

Post templates of the workspace, newest first. The same templates as the Templates page in the app. Paginated with `page` and `per_page` (default 100). 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::TemplatesApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
opts = {
  page: 56, # Integer | Page number (1-based).
  per_page: 56 # Integer | Items per page, 1-100.
}

begin
  # List templates
  result = api_instance.list_templates(workspace_uuid, opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling TemplatesApi->list_templates: #{e}"
end
```

#### Using the list_templates_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListTemplates200Response>, Integer, Hash)> list_templates_with_http_info(workspace_uuid, opts)

```ruby
begin
  # List templates
  data, status_code, headers = api_instance.list_templates_with_http_info(workspace_uuid, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListTemplates200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling TemplatesApi->list_templates_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **page** | **Integer** | Page number (1-based). | [optional][default to 1] |
| **per_page** | **Integer** | Items per page, 1-100. | [optional][default to 100] |

### Return type

[**ListTemplates200Response**](ListTemplates200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_template

> <CreateTemplate201Response> update_template(workspace_uuid, template_id, template_input)

Update a template

Replaces the name and content of a template. Admins and members only (not viewers). 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::TemplatesApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
template_id = 'template_id_example' # String | The template `id`.
template_input = PostBoost::TemplateInput.new({name: 'name_example'}) # TemplateInput | 

begin
  # Update a template
  result = api_instance.update_template(workspace_uuid, template_id, template_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling TemplatesApi->update_template: #{e}"
end
```

#### Using the update_template_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateTemplate201Response>, Integer, Hash)> update_template_with_http_info(workspace_uuid, template_id, template_input)

```ruby
begin
  # Update a template
  data, status_code, headers = api_instance.update_template_with_http_info(workspace_uuid, template_id, template_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateTemplate201Response>
rescue PostBoost::ApiError => e
  puts "Error when calling TemplatesApi->update_template_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **template_id** | **String** | The template &#x60;id&#x60;. |  |
| **template_input** | [**TemplateInput**](TemplateInput.md) |  |  |

### Return type

[**CreateTemplate201Response**](CreateTemplate201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

