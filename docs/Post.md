# PostBoost::Post

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** |  |  |
| **uuid** | **String** |  |  |
| **status** | [**PostStatus**](PostStatus.md) |  |  |
| **publish_progress** | [**PublishProgress**](PublishProgress.md) | Only present while the post is publishing. | [optional] |
| **accounts** | [**Array&lt;Account&gt;**](Account.md) |  |  |
| **versions** | [**Array&lt;PostVersion&gt;**](PostVersion.md) |  |  |
| **tags** | [**Array&lt;Tag&gt;**](Tag.md) |  |  |
| **scheduled_at** | **Time** |  | [optional] |
| **published_at** | **Time** |  | [optional] |
| **created_at** | **Time** |  |  |
| **trashed** | **Boolean** |  |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::Post.new(
  id: null,
  uuid: null,
  status: null,
  publish_progress: null,
  accounts: null,
  versions: null,
  tags: null,
  scheduled_at: null,
  published_at: null,
  created_at: null,
  trashed: null
)
```

