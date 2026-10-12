# PostBoost::RecyclingRun

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** |  |  |
| **status** | **String** |  |  |
| **reason** | **String** | Why the run skipped or failed; on &#x60;created&#x60;, a note such as &#x60;x_skipped_identical_text&#x60;. |  |
| **source_post_uuid** | **String** |  |  |
| **created_post_uuid** | **String** |  |  |
| **created_at** | **Time** |  |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::RecyclingRun.new(
  id: null,
  status: null,
  reason: null,
  source_post_uuid: null,
  created_post_uuid: null,
  created_at: null
)
```

