# PostBoost::FreeToolCountCharactersResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **hashtags** | **Integer** | Hashtags in the text (Instagram allows 5 per post in PostBoost). | [optional] |
| **networks** | [**Array&lt;FreeToolCountCharactersResponseNetworksInner&gt;**](FreeToolCountCharactersResponseNetworksInner.md) |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolCountCharactersResponse.new(
  hashtags: null,
  networks: null
)
```

