# PostBoost::GetRemoteUploadStatus200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **status** | **String** |  |  |
| **progress** | **Integer** | Percent done. It stays &#x60;0&#x60; until the file is stored and is &#x60;100&#x60; once &#x60;status&#x60; is &#x60;completed&#x60;, so poll on &#x60;status&#x60;. |  |
| **media** | [**Media**](Media.md) | Present when &#x60;status&#x60; is &#x60;completed&#x60; (absent if the item was deleted before this poll). | [optional] |
| **error** | **String** | Why the download failed. Present when &#x60;status&#x60; is &#x60;failed&#x60;. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::GetRemoteUploadStatus200Response.new(
  status: null,
  progress: null,
  media: null,
  error: null
)
```

