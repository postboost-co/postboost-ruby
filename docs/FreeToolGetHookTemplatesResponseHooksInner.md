# PostBoost::FreeToolGetHookTemplatesResponseHooksInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **text** | **String** | The hook, with &#x60;{topic}&#x60; filled in when a topic was given. | [optional] |
| **template** | **String** | The template with its &#x60;{topic}&#x60; placeholder. | [optional] |
| **category** | **String** | Hook style. | [optional] |
| **networks** | **Array&lt;String&gt;** | Networks the hook suits. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolGetHookTemplatesResponseHooksInner.new(
  text: null,
  template: null,
  category: null,
  networks: null
)
```

