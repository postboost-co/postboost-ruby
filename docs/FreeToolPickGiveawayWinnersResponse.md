# PostBoost::FreeToolPickGiveawayWinnersResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **winners** | **Array&lt;String&gt;** | Entrant keys in the drawn order. | [optional] |
| **alternates** | **Array&lt;String&gt;** | Entrant keys drawn after the winners, in order. | [optional] |
| **entrants_before** | **Integer** | Comments received. | [optional] |
| **entrants_after** | **Integer** | Entries left after the filters: the length of entrant_list. | [optional] |
| **entrant_list** | **Array&lt;String&gt;** | The canonical entrant list to publish: keys sorted by UTF-8 bytes. Joined with \&quot;\\n\&quot; it is what entrants_hash hashes. | [optional] |
| **entrants_hash** | **String** | SHA-256 (hex) of the canonical entrant list. | [optional] |
| **fingerprint** | **String** | SHA-256 (hex) of the seed bytes: what to publish before the entries close. | [optional] |
| **seed** | **String** | The seed used, lowercase hex. Publish it after the draw. | [optional] |
| **pre_committed** | **Boolean** | False when the seed was generated for this draw, so no fingerprint could be published before it. | [optional] |
| **algorithm** | **String** |  | [optional] |
| **warnings** | [**Array&lt;FreeToolCheckPostResponseNetworksInnerErrorsInner&gt;**](FreeToolCheckPostResponseNetworksInnerErrorsInner.md) | Codes: not_enough_entrants, not_pre_committed. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolPickGiveawayWinnersResponse.new(
  winners: null,
  alternates: null,
  entrants_before: null,
  entrants_after: null,
  entrant_list: null,
  entrants_hash: null,
  fingerprint: null,
  seed: null,
  pre_committed: null,
  algorithm: null,
  warnings: null
)
```

