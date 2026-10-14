# PostBoost::FreeToolFormatLinkedInPostRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **text** | **String** |  |  |
| **style** | **String** | Unicode style for the whole text, e.g. bold. | [optional] |
| **list** | **String** | Prefix every non-empty line with \&quot;• \&quot; or \&quot;1. \&quot;, \&quot;2. \&quot; (plain digits). | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolFormatLinkedInPostRequest.new(
  text: null,
  style: null,
  list: null
)
```

