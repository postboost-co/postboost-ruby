# PostBoost::FreeToolGetGlossaryResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **total** | **Integer** | Number of terms returned. | [optional] |
| **terms** | [**Array&lt;FreeToolGetGlossaryResponseTermsInner&gt;**](FreeToolGetGlossaryResponseTermsInner.md) |  | [optional] |
| **last_verified** | **Date** | When the definitions were last checked against their sources. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolGetGlossaryResponse.new(
  total: null,
  terms: null,
  last_verified: null
)
```

