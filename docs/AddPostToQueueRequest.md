# PostBoost::AddPostToQueueRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **timezone** | **String** | Accepted and validated for consistency with the other scheduling endpoints; queue slots are always taken from the workspace posting schedule. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::AddPostToQueueRequest.new(
  timezone: America/New_York
)
```

