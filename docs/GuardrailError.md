# PostBoost::GuardrailError

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **message** | **String** |  |  |
| **code** | **String** |  | [optional] |
| **account_id** | **Integer** | The account the problem is about. | [optional] |
| **existing_post_uuid** | **String** | &#x60;duplicate_post&#x60; only: the earlier post with the same content. | [optional] |
| **limit** | **Integer** | &#x60;account_daily_cap_reached&#x60; only: the account&#39;s daily cap. | [optional] |
| **used** | **Integer** | &#x60;account_daily_cap_reached&#x60; only: posts already counted on that UTC day. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::GuardrailError.new(
  message: null,
  code: null,
  account_id: null,
  existing_post_uuid: null,
  limit: null,
  used: null
)
```

