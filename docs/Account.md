# PostBoost::Account

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** |  | [optional] |
| **uuid** | **String** |  | [optional] |
| **name** | **String** |  | [optional] |
| **username** | **String** |  | [optional] |
| **image** | **String** |  | [optional] |
| **provider** | **String** |  | [optional] |
| **data** | **Object** | Provider-specific metadata. | [optional] |
| **authorized** | **Boolean** |  | [optional] |
| **created_at** | **Time** |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::Account.new(
  id: null,
  uuid: null,
  name: My Instagram,
  username: myhandle,
  image: null,
  provider: null,
  data: null,
  authorized: null,
  created_at: null
)
```

