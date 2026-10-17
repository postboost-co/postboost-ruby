# PostBoost::PreflightResult

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **valid** | **Boolean** | True when create-post with the same body would succeed. Warnings do not change it. |  |
| **errors** | **Hash&lt;String, Array&lt;String&gt;&gt;** | Validation and network-requirement errors keyed by field, as create-post would report them in a &#x60;422&#x60;. |  |
| **issues** | [**Array&lt;GuardrailError&gt;**](GuardrailError.md) | Guardrail problems, in the order create-post would report the first of them. |  |
| **warnings** | [**Array&lt;PostWarning&gt;**](PostWarning.md) | The warnings create-post would return for the same body (same codes and messages); empty when there are none. |  |
| **publish_at** | **Time** | UTC time the post would publish at; null for a draft. |  |
| **accounts** | [**Array&lt;AccountHealth&gt;**](AccountHealth.md) |  |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::PreflightResult.new(
  valid: null,
  errors: null,
  issues: null,
  warnings: null,
  publish_at: null,
  accounts: null
)
```

