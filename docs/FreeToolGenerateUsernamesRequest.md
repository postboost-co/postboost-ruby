# PostBoost::FreeToolGenerateUsernamesRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | Your name, brand or a few keywords. Accents are dropped; only Latin letters and digits are used. |  |
| **network** | **String** | Whose username rules apply (Threads uses your Instagram username). | [optional][default to &#39;instagram&#39;] |
| **style** | **String** | Which word list to mix in. | [optional][default to &#39;clean&#39;] |
| **numbers** | **Boolean** | Allow a number at the end of some names. | [optional][default to false] |
| **seed** | **Integer** | The same input and seed give the same list; change it for more ideas. | [optional][default to 0] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolGenerateUsernamesRequest.new(
  name: null,
  network: null,
  style: null,
  numbers: null,
  seed: null
)
```

