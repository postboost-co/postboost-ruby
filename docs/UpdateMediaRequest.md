# PostBoost::UpdateMediaRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  | [optional] |
| **alt_text** | **String** | Alternative text for accessibility. | [optional] |
| **folder** | **String** | UUID of the media folder to move the item to, or null for the library root. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::UpdateMediaRequest.new(
  name: null,
  alt_text: null,
  folder: null
)
```

