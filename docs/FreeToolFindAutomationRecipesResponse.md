# PostBoost::FreeToolFindAutomationRecipesResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **total** | **Integer** | Number of recipes returned. | [optional] |
| **recipes** | [**Array&lt;FreeToolFindAutomationRecipesResponseRecipesInner&gt;**](FreeToolFindAutomationRecipesResponseRecipesInner.md) |  | [optional] |
| **last_verified** | **Date** | When the recipes were last checked against the API and the platforms. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolFindAutomationRecipesResponse.new(
  total: null,
  recipes: null,
  last_verified: null
)
```

