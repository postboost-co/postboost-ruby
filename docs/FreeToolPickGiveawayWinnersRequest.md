# PostBoost::FreeToolPickGiveawayWinnersRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **entrants** | [**Array&lt;FreeToolPickGiveawayWinnersRequestEntrantsInner&gt;**](FreeToolPickGiveawayWinnersRequestEntrantsInner.md) | The comments, one item each. The request body is capped at 128 KB. |  |
| **seed** | **String** | The secret seed, 64 hex characters (32 bytes), whose fingerprint you published before the entries closed. Without it, a seed is generated and pre_committed is false. The steps of the draw (pb-draw-v1) and a test vector are on the web tool page. | [optional] |
| **one_per_person** | **Boolean** | Count each username once. Off: every comment is an entry, so one person can win more than once. | [optional][default to true] |
| **keywords** | **Array&lt;String&gt;** | Keep only comments that contain at least one of these, case-insensitive. | [optional] |
| **min_mentions** | **Integer** | Keep only comments that tag at least this many other @handles. | [optional][default to 0] |
| **exclude** | **Array&lt;String&gt;** | Usernames to leave out of the draw, such as the host account. | [optional] |
| **winners** | **Integer** |  | [optional][default to 1] |
| **alternates** | **Integer** | Runners-up drawn after the winners, in order. | [optional][default to 0] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolPickGiveawayWinnersRequest.new(
  entrants: null,
  seed: null,
  one_per_person: null,
  keywords: null,
  min_mentions: null,
  exclude: null,
  winners: null,
  alternates: null
)
```

