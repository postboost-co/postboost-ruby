# PostBoost::FreeToolVerifyWebhookSignatureResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **valid** | **Boolean** |  | [optional] |
| **expected** | **String** | The signature the body and secret give, with the prefix. | [optional] |
| **hints** | **Array&lt;String&gt;** | When invalid: the usual mistakes that would make it valid, each checked. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolVerifyWebhookSignatureResponse.new(
  valid: null,
  expected: null,
  hints: null
)
```

