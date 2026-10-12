# PostBoost::AccountGroupInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  |  |
| **accounts** | **Array&lt;Integer&gt;** | Account &#x60;id&#x60;s of this workspace. Replaces the group&#39;s accounts. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::AccountGroupInput.new(
  name: null,
  accounts: null
)
```

