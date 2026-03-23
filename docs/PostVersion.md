# PostBoost::PostVersion

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | Use &#x60;0&#x60; for the original/default version. |  |
| **is_original** | **Boolean** | Must be &#x60;true&#x60; for the first version. |  |
| **content** | [**Array&lt;PostContent&gt;**](PostContent.md) |  |  |
| **options** | **Object** | Platform-specific publishing options. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::PostVersion.new(
  account_id: null,
  is_original: null,
  content: null,
  options: null
)
```

