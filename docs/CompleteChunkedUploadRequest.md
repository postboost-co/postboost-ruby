# PostBoost::CompleteChunkedUploadRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **alt_text** | **String** |  | [optional] |
| **folder** | **String** | UUID of the media folder to file the item in. Omit or null for the library root. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::CompleteChunkedUploadRequest.new(
  alt_text: null,
  folder: null
)
```

