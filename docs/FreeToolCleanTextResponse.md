# PostBoost::FreeToolCleanTextResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **text** | **String** |  | [optional] |
| **changes** | [**Array&lt;FreeToolCleanTextResponseChangesInner&gt;**](FreeToolCleanTextResponseChangesInner.md) | One entry per change type that changed something. | [optional] |
| **flags** | [**Array&lt;FreeToolCleanTextResponseFlagsInner&gt;**](FreeToolCleanTextResponseFlagsInner.md) | AI phrases in the cleaned text, by offset (Unicode code points). | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolCleanTextResponse.new(
  text: null,
  changes: null,
  flags: null
)
```

