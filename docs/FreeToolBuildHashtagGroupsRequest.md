# PostBoost::FreeToolBuildHashtagGroupsRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **text** | **String** | Hashtags or words, separated by spaces, commas or new lines. A missing # is added. |  |
| **network** | **String** | Network whose hashtag cap applies. | [optional][default to &#39;instagram&#39;] |
| **group_size** | **Integer** | Hashtags per group. Default: the network&#39;s cap, or 5 when it has no hard cap. | [optional] |
| **_case** | **String** | keep the first spelling of each hashtag, or lower-case all of them. | [optional][default to &#39;keep&#39;] |
| **format** | **String** | inline: one line of tags. first_comment: five \&quot;.\&quot; lines, then the tags. | [optional][default to &#39;inline&#39;] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolBuildHashtagGroupsRequest.new(
  text: null,
  network: null,
  group_size: null,
  _case: null,
  format: null
)
```

