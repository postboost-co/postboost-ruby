# PostBoost::FreeToolGenerateBrandVoiceRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **posts** | **Array&lt;String&gt;** | Your own posts, one per item: 3 to 10 different posts of 20 to 3,200 characters, 20,000 in total. An exact copy counts once. |  |
| **business_name** | **String** | Your business name, used as given (never generated). | [optional] |
| **industry** | **String** | Your industry, used as given (never generated). | [optional] |
| **workspace** | **String** | UUID of the workspace whose AI credits pay for the call. Default: your active workspace (a scoped API key: its own workspace). | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolGenerateBrandVoiceRequest.new(
  posts: null,
  business_name: null,
  industry: null,
  workspace: null
)
```

