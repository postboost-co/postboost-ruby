# PostBoost::TemplateInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  |  |
| **content** | [**Array&lt;TemplateInputContentInner&gt;**](TemplateInputContentInner.md) | One item per post in a thread; usually one. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::TemplateInput.new(
  name: null,
  content: null
)
```

