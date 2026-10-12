# PostBoost::ApiActivity

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** |  |  |
| **user_id** | **Integer** |  | [optional] |
| **token_ref** | **String** | First 12 hex characters of the SHA-256 of the API token used, to tell tokens apart. | [optional] |
| **client** | **String** | &#x60;X-PostBoost-Client&#x60; header, else the &#x60;User-Agent&#x60;. | [optional] |
| **route_name** | **String** |  | [optional] |
| **method** | **String** |  |  |
| **post_uuid** | **String** |  | [optional] |
| **outcome** | [**ApiActivityOutcome**](ApiActivityOutcome.md) |  |  |
| **http_status** | **Integer** |  |  |
| **created_at** | **Time** |  |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::ApiActivity.new(
  id: null,
  user_id: null,
  token_ref: null,
  client: null,
  route_name: null,
  method: null,
  post_uuid: null,
  outcome: null,
  http_status: null,
  created_at: null
)
```

