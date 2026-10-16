# PostBoost::Media

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Numeric media id, returned as a string (the engine casts it). Use &#x60;uuid&#x60; to address media in the API. |  |
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
| **created_at** | **String** | &#x60;Y-m-d H:i:s&#x60; in UTC (not RFC 3339). |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::Media.new(
  id: 42,
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
  created_at: 2026-10-16 05:30:00
)
```

