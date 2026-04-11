# PostBoost::ImageAltTextResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **media_uuid** | **String** |  |  |
| **alt_text** | **String** |  |  |
| **credits_used** | **Integer** |  |  |
| **credits_remaining** | **Integer** |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::ImageAltTextResponse.new(
  media_uuid: null,
  alt_text: A developer working at a standing desk with dual monitors in a bright modern office,
  credits_used: 1,
  credits_remaining: 49
)
```

