# PostBoost::Post

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** |  | [optional] |
| **uuid** | **String** |  | [optional] |
| **status** | [**PostStatus**](PostStatus.md) |  | [optional] |
| **accounts** | [**Array&lt;Account&gt;**](Account.md) |  | [optional] |
| **versions** | [**Array&lt;PostVersion&gt;**](PostVersion.md) |  | [optional] |
| **tags** | [**Array&lt;Tag&gt;**](Tag.md) |  | [optional] |
| **scheduled_at** | **Time** |  | [optional] |
| **published_at** | **Time** |  | [optional] |
| **created_at** | **Time** |  | [optional] |
| **trashed** | **Boolean** |  | [optional] |

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

