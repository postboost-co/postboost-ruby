# PostBoost::FreeToolCountCharactersRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **text** | **String** | The post text, up to 10,000 characters (twice the longest network limit). | [optional][default to &#39;&#39;] |
| **network** | **String** | Count for one network only; all networks when omitted. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolCountCharactersRequest.new(
  text: null,
  network: null
)
```

