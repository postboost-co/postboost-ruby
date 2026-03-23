# PostBoost::GetRemoteUploadStatus200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **status** | **String** |  | [optional] |
| **media** | [**Media**](Media.md) | Present when status is complete. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::GetRemoteUploadStatus200Response.new(
  status: null,
  media: null
)
```

