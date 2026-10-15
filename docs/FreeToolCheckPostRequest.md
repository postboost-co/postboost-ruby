# PostBoost::FreeToolCheckPostRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **text** | **String** | The post text, up to 10,000 characters; 5,000 without an API token. | [optional][default to &#39;&#39;] |
| **networks** | **Array&lt;String&gt;** | The networks to check the post for. |  |
| **media** | [**FreeToolCheckPostRequestMedia**](FreeToolCheckPostRequestMedia.md) |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolCheckPostRequest.new(
  text: null,
  networks: null,
  media: null
)
```

