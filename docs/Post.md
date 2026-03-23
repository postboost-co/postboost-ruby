# PostBoost::Post

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** |  |  |
| **uuid** | **String** |  |  |
| **status** | [**PostStatus**](PostStatus.md) |  |  |
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
  accounts: null,
  versions: null,
  tags: null,
  scheduled_at: null,
  published_at: null,
  created_at: null,
  trashed: null
)
```

