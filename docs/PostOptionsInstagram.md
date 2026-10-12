# PostBoost::PostOptionsInstagram

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  | [optional][default to &#39;post&#39;] |
| **collaborators** | **Array&lt;String&gt;** | Usernames invited as collaborators (not for stories). | [optional] |
| **ai_generated** | **Boolean** | Instagram&#39;s \&quot;AI info\&quot; label on the post (on the carousel itself for carousels; not for stories). Set by &#x60;ai_generated&#x60;. | [optional][default to false] |

## Example

```ruby
require 'postboost'

instance = PostBoost::PostOptionsInstagram.new(
  type: null,
  collaborators: null,
  ai_generated: null
)
```

