# PostBoost::BlogToSocialMedia

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** | Media library ID of the imported image. | [optional] |
| **url** | **String** | Public URL of the imported image in the workspace media library. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::BlogToSocialMedia.new(
  id: 42,
  url: https://postboost.co/storage/workspaces/1/blog-images/2026/04/cover.jpg
)
```

