# PostBoost::FreeToolFormatCrossPostRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **text** | **String** | The post text, up to 10,000 characters. | [optional][default to &#39;&#39;] |
| **networks** | **Array&lt;String&gt;** | The networks to format for, in the order the result lists them. | [optional] |
| **numbering** | **Boolean** | End each post of a thread with \&quot; k/n\&quot;. | [optional][default to false] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolFormatCrossPostRequest.new(
  text: null,
  networks: null,
  numbering: null
)
```

