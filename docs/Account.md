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
| **profile_url** | **String** | Public URL of the account&#39;s profile on the network, when known. | [optional] |
| **publish_status** | **String** | Only present when the account is embedded in a post. Publishing state of this account for the post. | [optional] |
| **published_parts** | **Integer** | Only present when the account is embedded in a post. How many parts (for example thread items or a first comment) are live on the network. | [optional] |
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
  profile_url: null,
  publish_status: null,
  published_parts: null,
  created_at: null
)
```

