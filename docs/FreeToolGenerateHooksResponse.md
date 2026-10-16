# PostBoost::FreeToolGenerateHooksResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **hooks** | [**Array&lt;FreeToolGenerateHooksResponseHooksInner&gt;**](FreeToolGenerateHooksResponseHooksInner.md) | &#x60;count&#x60; hooks in several styles. | [optional] |
| **notice** | **String** | Only while AI is switched off: the hooks are templates from the free library (getHookTemplates) with the topic filled in, free of charge. | [optional] |
| **credits_spent** | **Integer** | AI credits this call took from the workspace: 1, or 0 for a cached result. | [optional] |
| **cached** | **Boolean** | True when the same request was answered before (free). | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolGenerateHooksResponse.new(
  hooks: null,
  notice: null,
  credits_spent: null,
  cached: null
)
```

