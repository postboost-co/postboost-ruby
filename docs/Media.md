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
  created_at: null
)
```

