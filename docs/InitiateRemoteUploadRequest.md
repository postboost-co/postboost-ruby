# PostBoost::InitiateRemoteUploadRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **url** | **String** | URL of the remote file to download. |  |
| **alt_text** | **String** |  | [optional] |
| **folder** | **String** | UUID of the media folder to file the item in. Omit or null for the library root. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::InitiateRemoteUploadRequest.new(
  url: null,
  alt_text: null,
  folder: null
)
```

