# PostBoost::FreeToolFormatCrossPostResponseNetworksInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **key** | **String** |  | [optional] |
| **label** | **String** |  | [optional] |
| **limit** | **Integer** |  | [optional] |
| **count** | **Integer** | Length as the network counts it. | [optional] |
| **fits** | **Boolean** |  | [optional] |
| **over_by** | **Integer** | Characters over the limit; 0 when it fits. | [optional] |
| **links** | **Integer** | Unique http(s) links in the text (trailing punctuation trimmed), as Threads counts them. | [optional] |
| **warnings** | [**Array&lt;FreeToolCheckPostResponseNetworksInnerErrorsInner&gt;**](FreeToolCheckPostResponseNetworksInnerErrorsInner.md) | Codes: threads_too_many_links, cut_by_fold, mentions_not_portable. | [optional] |
| **thread** | [**Array&lt;FreeToolFormatCrossPostResponseNetworksInnerThreadInner&gt;**](FreeToolFormatCrossPostResponseNetworksInnerThreadInner.md) | The thread for a text that does not fit (X, Threads, Bluesky, Mastodon); null when it fits or on LinkedIn. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolFormatCrossPostResponseNetworksInner.new(
  key: null,
  label: null,
  limit: null,
  count: null,
  fits: null,
  over_by: null,
  links: null,
  warnings: null,
  thread: null
)
```

