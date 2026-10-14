# PostBoost::RepurposeRun

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **run_id** | **Integer** |  |  |
| **status** | **String** |  |  |
| **error** | **String** | Why the run failed. |  |
| **post_uuid** | **String** | The draft post, once created. |  |
| **credits_used** | **Integer** |  |  |
| **result** | [**RepurposeResult**](RepurposeResult.md) |  |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::RepurposeRun.new(
  run_id: null,
  status: null,
  error: null,
  post_uuid: null,
  credits_used: null,
  result: null
)
```

