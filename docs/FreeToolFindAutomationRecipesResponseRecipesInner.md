# PostBoost::FreeToolFindAutomationRecipesResponseRecipesInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **slug** | **String** | Stable key of the recipe, also its anchor on the page. | [optional] |
| **title** | **String** | What the recipe does. | [optional] |
| **trigger** | **String** | What starts it. | [optional] |
| **goal** | **String** | The result in one or two sentences. | [optional] |
| **native** | [**FreeToolFindAutomationRecipesResponseRecipesInnerNative**](FreeToolFindAutomationRecipesResponseRecipesInnerNative.md) |  | [optional] |
| **api_operations** | [**Array&lt;FreeToolFindAutomationRecipesResponseRecipesInnerApiOperationsInner&gt;**](FreeToolFindAutomationRecipesResponseRecipesInnerApiOperationsInner.md) | The PostBoost API operations the recipe calls. | [optional] |
| **steps** | [**FreeToolFindAutomationRecipesResponseRecipesInnerSteps**](FreeToolFindAutomationRecipesResponseRecipesInnerSteps.md) |  | [optional] |
| **n8n_workflow** | **Hash&lt;String, Object&gt;** | Importable n8n workflow (core nodes only; add a Header Auth credential named \&quot;PostBoost API token\&quot;) when &#x60;platform&#x60; is &#x60;n8n&#x60;; null otherwise. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolFindAutomationRecipesResponseRecipesInner.new(
  slug: null,
  title: null,
  trigger: null,
  goal: null,
  native: null,
  api_operations: null,
  steps: null,
  n8n_workflow: null
)
```

