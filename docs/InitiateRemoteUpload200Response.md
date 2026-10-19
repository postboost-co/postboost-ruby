# PostBoost::InitiateRemoteUpload200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **status** | **String** | &#x60;completed&#x60; and &#x60;failed&#x60; are final; &#x60;pending&#x60; means the file downloads in the background. |  |
| **media** | [**Media**](Media.md) | Present when &#x60;status&#x60; is &#x60;completed&#x60;. This copy has no &#x60;size&#x60;; &#x60;getMedia&#x60; returns it. | [optional] |
| **error** | **String** | Why the download failed. Present when &#x60;status&#x60; is &#x60;failed&#x60;. | [optional] |
| **download_id** | **String** | Present when &#x60;status&#x60; is &#x60;pending&#x60;. Pass it to &#x60;getRemoteUploadStatus&#x60;. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::InitiateRemoteUpload200Response.new(
  status: null,
  media: null,
  error: null,
  download_id: null
)
```

