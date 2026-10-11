# PostBoost::Media

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** |  |  |
| **uuid** | **String** |  |  |
| **name** | **String** |  |  |
| **mime_type** | **String** |  |  |
| **type** | **String** |  |  |
| **url** | **String** |  |  |
| **thumb_url** | **String** |  | [optional] |
| **is_video** | **Boolean** |  |  |
| **is_processing** | **Boolean** | True while an uploaded video is still being converted. | [optional] |
| **width** | **Integer** | Width in pixels, when stored. | [optional] |
| **height** | **Integer** | Height in pixels, when stored. | [optional] |
| **duration_ms** | **Integer** | Video duration in milliseconds; null for images or videos not read yet. | [optional] |
| **size** | **Integer** | File size in bytes. | [optional] |
| **alt_text** | **String** |  | [optional] |
| **folder** | [**MediaFolderRef**](MediaFolderRef.md) |  | [optional] |
| **created_at** | **Time** |  |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::Media.new(
  id: null,
  uuid: null,
  name: null,
  mime_type: image/jpeg,
  type: null,
  url: null,
  thumb_url: null,
  is_video: null,
  is_processing: null,
  width: null,
  height: null,
  duration_ms: null,
  size: null,
  alt_text: null,
  folder: null,
  created_at: null
)
```

