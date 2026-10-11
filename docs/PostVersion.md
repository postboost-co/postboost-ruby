# PostBoost::PostVersion

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | Use &#x60;0&#x60; for the original/default version. |  |
| **is_original** | **Boolean** | Must be &#x60;true&#x60; for the first version. |  |
| **synced_with** | **Integer** | Account ID of the version this version follows (&#x60;0&#x60; &#x3D; the original), or null when it is edited independently. Ignored on the original version. | [optional] |
| **content** | [**Array&lt;PostContent&gt;**](PostContent.md) |  |  |
| **options** | **Object** | Platform-specific publishing options. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::PostVersion.new(
  account_id: null,
  is_original: null,
  synced_with: null,
  content: null,
  options: null
)
```

