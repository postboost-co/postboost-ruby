# PostBoost::DeletePostRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **trash** | **Boolean** |  | [optional][default to false] |
| **delete_mode** | [**DeleteMode**](DeleteMode.md) |  | [optional][default to &#39;app_only&#39;] |

## Example

```ruby
require 'postboost'

instance = PostBoost::DeletePostRequest.new(
  trash: null,
  delete_mode: null
)
```

