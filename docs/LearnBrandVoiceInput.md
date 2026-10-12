# PostBoost::LearnBrandVoiceInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **limit** | **Integer** | How many of the latest published posts to read. | [optional][default to 10] |
| **account_ids** | **Array&lt;Integer&gt;** | Only read posts whose accounts are all among these. | [optional] |
| **apply** | **Boolean** | Save the proposed voice as the workspace brand voice. | [optional][default to false] |
| **overwrite** | **Boolean** | Let learned values replace fields that are already set. | [optional][default to false] |

## Example

```ruby
require 'postboost'

instance = PostBoost::LearnBrandVoiceInput.new(
  limit: null,
  account_ids: null,
  apply: null,
  overwrite: null
)
```

