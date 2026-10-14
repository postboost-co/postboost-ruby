# PostBoost::FreeToolSplitThreadRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **text** | **String** | The long text, up to 10,000 characters. A line with only --- forces a new post. | [optional][default to &#39;&#39;] |
| **network** | **String** |  | [optional][default to &#39;x&#39;] |
| **numbering** | **Boolean** | End each post with \&quot; k/n\&quot;. | [optional][default to false] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolSplitThreadRequest.new(
  text: null,
  network: null,
  numbering: null
)
```

