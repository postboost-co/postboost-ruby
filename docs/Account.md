# PostBoost::Account

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** |  |  |
| **uuid** | **String** |  |  |
| **name** | **String** |  |  |
| **username** | **String** |  |  |
| **image** | **String** |  | [optional] |
| **provider** | **String** |  |  |
| **data** | **Object** | Provider-specific metadata. |  |
| **authorized** | **Boolean** |  |  |
| **created_at** | **Time** |  |  |

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

