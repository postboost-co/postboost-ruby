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
| **scheduled_at** | **String** | &#x60;Y-m-d H:i:s&#x60; in UTC (not RFC 3339). | [optional] |
| **published_at** | **String** | &#x60;Y-m-d H:i:s&#x60; in UTC (not RFC 3339). | [optional] |
| **created_at** | **String** | &#x60;Y-m-d H:i:s&#x60; in UTC (not RFC 3339). |  |
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
  scheduled_at: 2026-10-16 10:00:00,
  published_at: 2026-10-16 10:00:04,
  created_at: 2026-10-16 09:58:12,
  trashed: null
)
```

