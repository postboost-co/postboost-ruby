# PostBoost::FreeToolGenerateSocialPostsFromBlogResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **posts** | [**Array&lt;FreeToolGenerateSocialPostsFromBlogResponsePostsInner&gt;**](FreeToolGenerateSocialPostsFromBlogResponsePostsInner.md) | One post per platform that came back, in the order asked. | [optional] |
| **source** | [**FreeToolGenerateSocialPostsFromBlogResponseSource**](FreeToolGenerateSocialPostsFromBlogResponseSource.md) |  | [optional] |
| **warnings** | [**Array&lt;FreeToolGenerateSocialPostsFromBlogResponseWarningsInner&gt;**](FreeToolGenerateSocialPostsFromBlogResponseWarningsInner.md) |  | [optional] |
| **credits_spent** | **Integer** | AI credits this call took from the workspace: one per post. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolGenerateSocialPostsFromBlogResponse.new(
  posts: null,
  source: null,
  warnings: null,
  credits_spent: null
)
```

