# PostBoost::FreeToolGenerateSocialPostsFromBlogRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **url** | **String** | Public http(s) address of the blog post. Give &#x60;url&#x60; or &#x60;text&#x60;. | [optional] |
| **text** | **String** | The blog post itself, instead of &#x60;url&#x60;. | [optional] |
| **platforms** | **Array&lt;String&gt;** | Networks to write for, at most 4 per call (one AI credit each). |  |
| **tone** | **String** |  | [optional][default to &#39;casual&#39;] |
| **length** | **String** |  | [optional][default to &#39;short&#39;] |
| **hashtags** | **String** | How many hashtags to include. | [optional][default to &#39;no&#39;] |
| **cta** | **String** | Call to action to end with. | [optional][default to &#39;no&#39;] |
| **workspace** | **String** | UUID of the workspace whose AI credits pay for the call. Default: your active workspace (a scoped API key: its own workspace). | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolGenerateSocialPostsFromBlogRequest.new(
  url: null,
  text: null,
  platforms: null,
  tone: null,
  length: null,
  hashtags: null,
  cta: null,
  workspace: null
)
```

