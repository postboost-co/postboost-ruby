# PostBoost::Mention

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **reference** | **Integer** | Write &#x60;{{mention:&lt;reference&gt;}}&#x60; in a post body to mention this entry; it is resolved to each network&#39;s identity at publish time. |  |
| **name** | **String** |  |  |
| **avatar** | **String** |  | [optional] |
| **identities** | [**Array&lt;MentionIdentity&gt;**](MentionIdentity.md) |  | [optional] |
| **created_at** | **Time** |  |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::Mention.new(
  id: null,
  reference: null,
  name: Jane Doe,
  avatar: null,
  identities: null,
  created_at: null
)
```

