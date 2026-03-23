# PostBoost::InitiateChunkedUploadRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **filename** | **String** |  |  |
| **mime_type** | **String** |  |  |
| **total_size** | **Integer** | Total file size in bytes. |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::InitiateChunkedUploadRequest.new(
  filename: null,
  mime_type: video/mp4,
  total_size: null
)
```

