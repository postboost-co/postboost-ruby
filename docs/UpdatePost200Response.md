# PostBoost::UpdatePost200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **warnings** | [**Array&lt;PostWarning&gt;**](PostWarning.md) | Present only when there is at least one warning. | [optional] |
| **success** | **Boolean** |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::UpdatePost200Response.new(
  warnings: null,
  success: true
)
```

