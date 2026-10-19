# PostBoost::FreeToolGenerateUsernamesResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **network** | **String** |  | [optional] |
| **style** | **String** |  | [optional] |
| **seed** | **Integer** |  | [optional] |
| **usernames** | [**Array&lt;FreeToolGenerateUsernamesResponseUsernamesInner&gt;**](FreeToolGenerateUsernamesResponseUsernamesInner.md) | Up to 30 names, each valid for the network. Not checked for availability: open the profile URL to see whether a name is taken. | [optional] |
| **rules** | [**FreeToolGenerateUsernamesResponseRules**](FreeToolGenerateUsernamesResponseRules.md) |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolGenerateUsernamesResponse.new(
  network: null,
  style: null,
  seed: null,
  usernames: null,
  rules: null
)
```

