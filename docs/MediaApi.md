# PostBoost::MediaApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**abort_chunked_upload**](MediaApi.md#abort_chunked_upload) | **DELETE** /{workspaceUuid}/media/chunked/{uploadUuid} | Abort chunked upload |
| [**complete_chunked_upload**](MediaApi.md#complete_chunked_upload) | **POST** /{workspaceUuid}/media/chunked/{uploadUuid}/complete | Complete chunked upload |
| [**delete_media_bulk**](MediaApi.md#delete_media_bulk) | **DELETE** /{workspaceUuid}/media | Delete media (bulk) |
| [**get_media**](MediaApi.md#get_media) | **GET** /{workspaceUuid}/media/{mediaUuid} | Get media |
| [**get_remote_upload_status**](MediaApi.md#get_remote_upload_status) | **GET** /{workspaceUuid}/media/remote/{downloadId}/status | Get remote upload status |
| [**initiate_chunked_upload**](MediaApi.md#initiate_chunked_upload) | **POST** /{workspaceUuid}/media/chunked/initiate | Initiate chunked upload |
| [**initiate_remote_upload**](MediaApi.md#initiate_remote_upload) | **POST** /{workspaceUuid}/media/remote/initiate | Initiate remote upload |
| [**list_media**](MediaApi.md#list_media) | **GET** /{workspaceUuid}/media | List media |
| [**update_media**](MediaApi.md#update_media) | **PUT** /{workspaceUuid}/media/{mediaUuid} | Update media |
| [**upload_chunk**](MediaApi.md#upload_chunk) | **POST** /{workspaceUuid}/media/chunked/{uploadUuid}/upload | Upload a chunk |
| [**upload_media**](MediaApi.md#upload_media) | **POST** /{workspaceUuid}/media | Upload media (binary) |


## abort_chunked_upload

> abort_chunked_upload(workspace_uuid, upload_uuid)

Abort chunked upload

Cancel an in-progress chunked upload session and clean up uploaded chunks.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::MediaApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
upload_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  # Abort chunked upload
  api_instance.abort_chunked_upload(workspace_uuid, upload_uuid)
rescue PostBoost::ApiError => e
  puts "Error when calling MediaApi->abort_chunked_upload: #{e}"
end
```

#### Using the abort_chunked_upload_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> abort_chunked_upload_with_http_info(workspace_uuid, upload_uuid)

```ruby
begin
  # Abort chunked upload
  data, status_code, headers = api_instance.abort_chunked_upload_with_http_info(workspace_uuid, upload_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue PostBoost::ApiError => e
  puts "Error when calling MediaApi->abort_chunked_upload_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **upload_uuid** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## complete_chunked_upload

> <Media> complete_chunked_upload(workspace_uuid, upload_uuid)

Complete chunked upload

Signal that all chunks have been uploaded. Returns the final media object.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::MediaApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
upload_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  # Complete chunked upload
  result = api_instance.complete_chunked_upload(workspace_uuid, upload_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling MediaApi->complete_chunked_upload: #{e}"
end
```

#### Using the complete_chunked_upload_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Media>, Integer, Hash)> complete_chunked_upload_with_http_info(workspace_uuid, upload_uuid)

```ruby
begin
  # Complete chunked upload
  data, status_code, headers = api_instance.complete_chunked_upload_with_http_info(workspace_uuid, upload_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Media>
rescue PostBoost::ApiError => e
  puts "Error when calling MediaApi->complete_chunked_upload_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **upload_uuid** | **String** |  |  |

### Return type

[**Media**](Media.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## delete_media_bulk

> Object delete_media_bulk(workspace_uuid, delete_media_bulk_request)

Delete media (bulk)

Delete one or more media items by their IDs.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::MediaApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
delete_media_bulk_request = PostBoost::DeleteMediaBulkRequest.new({items: [37]}) # DeleteMediaBulkRequest | 

begin
  # Delete media (bulk)
  result = api_instance.delete_media_bulk(workspace_uuid, delete_media_bulk_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling MediaApi->delete_media_bulk: #{e}"
end
```

#### Using the delete_media_bulk_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> delete_media_bulk_with_http_info(workspace_uuid, delete_media_bulk_request)

```ruby
begin
  # Delete media (bulk)
  data, status_code, headers = api_instance.delete_media_bulk_with_http_info(workspace_uuid, delete_media_bulk_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue PostBoost::ApiError => e
  puts "Error when calling MediaApi->delete_media_bulk_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **delete_media_bulk_request** | [**DeleteMediaBulkRequest**](DeleteMediaBulkRequest.md) |  |  |

### Return type

**Object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## get_media

> <Media> get_media(workspace_uuid, media_uuid)

Get media

Returns a single media asset.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::MediaApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
media_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the media asset.

begin
  # Get media
  result = api_instance.get_media(workspace_uuid, media_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling MediaApi->get_media: #{e}"
end
```

#### Using the get_media_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Media>, Integer, Hash)> get_media_with_http_info(workspace_uuid, media_uuid)

```ruby
begin
  # Get media
  data, status_code, headers = api_instance.get_media_with_http_info(workspace_uuid, media_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Media>
rescue PostBoost::ApiError => e
  puts "Error when calling MediaApi->get_media_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **media_uuid** | **String** | UUID of the media asset. |  |

### Return type

[**Media**](Media.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_remote_upload_status

> <GetRemoteUploadStatus200Response> get_remote_upload_status(workspace_uuid, download_id)

Get remote upload status

Poll the status of an in-progress remote media download.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::MediaApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
download_id = 'download_id_example' # String | 

begin
  # Get remote upload status
  result = api_instance.get_remote_upload_status(workspace_uuid, download_id)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling MediaApi->get_remote_upload_status: #{e}"
end
```

#### Using the get_remote_upload_status_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetRemoteUploadStatus200Response>, Integer, Hash)> get_remote_upload_status_with_http_info(workspace_uuid, download_id)

```ruby
begin
  # Get remote upload status
  data, status_code, headers = api_instance.get_remote_upload_status_with_http_info(workspace_uuid, download_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetRemoteUploadStatus200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling MediaApi->get_remote_upload_status_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **download_id** | **String** |  |  |

### Return type

[**GetRemoteUploadStatus200Response**](GetRemoteUploadStatus200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## initiate_chunked_upload

> <InitiateChunkedUpload200Response> initiate_chunked_upload(workspace_uuid, initiate_chunked_upload_request)

Initiate chunked upload

Start a chunked upload session for large files. Returns an `upload_uuid`, `chunk_size`, and `total_chunks` to use for subsequent chunk requests. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::MediaApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
initiate_chunked_upload_request = PostBoost::InitiateChunkedUploadRequest.new({filename: 'filename_example', mime_type: 'video/mp4', total_size: 37}) # InitiateChunkedUploadRequest | 

begin
  # Initiate chunked upload
  result = api_instance.initiate_chunked_upload(workspace_uuid, initiate_chunked_upload_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling MediaApi->initiate_chunked_upload: #{e}"
end
```

#### Using the initiate_chunked_upload_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<InitiateChunkedUpload200Response>, Integer, Hash)> initiate_chunked_upload_with_http_info(workspace_uuid, initiate_chunked_upload_request)

```ruby
begin
  # Initiate chunked upload
  data, status_code, headers = api_instance.initiate_chunked_upload_with_http_info(workspace_uuid, initiate_chunked_upload_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <InitiateChunkedUpload200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling MediaApi->initiate_chunked_upload_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **initiate_chunked_upload_request** | [**InitiateChunkedUploadRequest**](InitiateChunkedUploadRequest.md) |  |  |

### Return type

[**InitiateChunkedUpload200Response**](InitiateChunkedUpload200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## initiate_remote_upload

> <InitiateRemoteUpload200Response> initiate_remote_upload(workspace_uuid, initiate_remote_upload_request)

Initiate remote upload

Download a file from a remote URL into the media library. For small files the media object is returned immediately. For large files a `download_id` is returned — poll the status endpoint. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::MediaApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
initiate_remote_upload_request = PostBoost::InitiateRemoteUploadRequest.new({url: 'url_example'}) # InitiateRemoteUploadRequest | 

begin
  # Initiate remote upload
  result = api_instance.initiate_remote_upload(workspace_uuid, initiate_remote_upload_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling MediaApi->initiate_remote_upload: #{e}"
end
```

#### Using the initiate_remote_upload_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<InitiateRemoteUpload200Response>, Integer, Hash)> initiate_remote_upload_with_http_info(workspace_uuid, initiate_remote_upload_request)

```ruby
begin
  # Initiate remote upload
  data, status_code, headers = api_instance.initiate_remote_upload_with_http_info(workspace_uuid, initiate_remote_upload_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <InitiateRemoteUpload200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling MediaApi->initiate_remote_upload_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **initiate_remote_upload_request** | [**InitiateRemoteUploadRequest**](InitiateRemoteUploadRequest.md) |  |  |

### Return type

[**InitiateRemoteUpload200Response**](InitiateRemoteUpload200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## list_media

> <ListMedia200Response> list_media(workspace_uuid, opts)

List media

Returns a paginated list of media assets in the workspace library.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::MediaApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
opts = {
  page: 56 # Integer | Page number (20 items per page).
}

begin
  # List media
  result = api_instance.list_media(workspace_uuid, opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling MediaApi->list_media: #{e}"
end
```

#### Using the list_media_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListMedia200Response>, Integer, Hash)> list_media_with_http_info(workspace_uuid, opts)

```ruby
begin
  # List media
  data, status_code, headers = api_instance.list_media_with_http_info(workspace_uuid, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListMedia200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling MediaApi->list_media_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **page** | **Integer** | Page number (20 items per page). | [optional][default to 1] |

### Return type

[**ListMedia200Response**](ListMedia200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_media

> Object update_media(workspace_uuid, media_uuid, update_media_request)

Update media

Update the alt text of a media asset.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::MediaApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
media_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the media asset.
update_media_request = PostBoost::UpdateMediaRequest.new({alt_text: 'alt_text_example'}) # UpdateMediaRequest | 

begin
  # Update media
  result = api_instance.update_media(workspace_uuid, media_uuid, update_media_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling MediaApi->update_media: #{e}"
end
```

#### Using the update_media_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> update_media_with_http_info(workspace_uuid, media_uuid, update_media_request)

```ruby
begin
  # Update media
  data, status_code, headers = api_instance.update_media_with_http_info(workspace_uuid, media_uuid, update_media_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue PostBoost::ApiError => e
  puts "Error when calling MediaApi->update_media_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **media_uuid** | **String** | UUID of the media asset. |  |
| **update_media_request** | [**UpdateMediaRequest**](UpdateMediaRequest.md) |  |  |

### Return type

**Object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## upload_chunk

> <UploadChunk200Response> upload_chunk(workspace_uuid, upload_uuid, chunk, chunk_index)

Upload a chunk

Upload a single chunk of a chunked upload session.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::MediaApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
upload_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
chunk = File.new('/path/to/some/file') # File | 
chunk_index = 56 # Integer | Zero-based index of this chunk.

begin
  # Upload a chunk
  result = api_instance.upload_chunk(workspace_uuid, upload_uuid, chunk, chunk_index)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling MediaApi->upload_chunk: #{e}"
end
```

#### Using the upload_chunk_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UploadChunk200Response>, Integer, Hash)> upload_chunk_with_http_info(workspace_uuid, upload_uuid, chunk, chunk_index)

```ruby
begin
  # Upload a chunk
  data, status_code, headers = api_instance.upload_chunk_with_http_info(workspace_uuid, upload_uuid, chunk, chunk_index)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UploadChunk200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling MediaApi->upload_chunk_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **upload_uuid** | **String** |  |  |
| **chunk** | **File** |  |  |
| **chunk_index** | **Integer** | Zero-based index of this chunk. |  |

### Return type

[**UploadChunk200Response**](UploadChunk200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json


## upload_media

> <Media> upload_media(workspace_uuid, file, opts)

Upload media (binary)

Upload a file directly as multipart form data.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::MediaApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
file = File.new('/path/to/some/file') # File | The file to upload.
opts = {
  alt_text: 'alt_text_example' # String | Alternative text for accessibility.
}

begin
  # Upload media (binary)
  result = api_instance.upload_media(workspace_uuid, file, opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling MediaApi->upload_media: #{e}"
end
```

#### Using the upload_media_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Media>, Integer, Hash)> upload_media_with_http_info(workspace_uuid, file, opts)

```ruby
begin
  # Upload media (binary)
  data, status_code, headers = api_instance.upload_media_with_http_info(workspace_uuid, file, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Media>
rescue PostBoost::ApiError => e
  puts "Error when calling MediaApi->upload_media_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **file** | **File** | The file to upload. |  |
| **alt_text** | **String** | Alternative text for accessibility. | [optional] |

### Return type

[**Media**](Media.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json

