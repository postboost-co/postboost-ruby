# PostBoost::FreeToolScoreSocialAuditRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **target_posts_per_week** | **Integer** | Your own posting target per network and week, used in the frequency question. | [optional][default to 3] |
| **instagram** | [**FreeToolScoreSocialAuditRequestInstagram**](FreeToolScoreSocialAuditRequestInstagram.md) |  | [optional] |
| **facebook** | [**FreeToolScoreSocialAuditRequestInstagram**](FreeToolScoreSocialAuditRequestInstagram.md) |  | [optional] |
| **linkedin** | [**FreeToolScoreSocialAuditRequestInstagram**](FreeToolScoreSocialAuditRequestInstagram.md) |  | [optional] |
| **x** | [**FreeToolScoreSocialAuditRequestInstagram**](FreeToolScoreSocialAuditRequestInstagram.md) |  | [optional] |
| **tiktok** | [**FreeToolScoreSocialAuditRequestInstagram**](FreeToolScoreSocialAuditRequestInstagram.md) |  | [optional] |
| **youtube** | [**FreeToolScoreSocialAuditRequestInstagram**](FreeToolScoreSocialAuditRequestInstagram.md) |  | [optional] |
| **pinterest** | [**FreeToolScoreSocialAuditRequestInstagram**](FreeToolScoreSocialAuditRequestInstagram.md) |  | [optional] |
| **threads** | [**FreeToolScoreSocialAuditRequestInstagram**](FreeToolScoreSocialAuditRequestInstagram.md) |  | [optional] |
| **bluesky** | [**FreeToolScoreSocialAuditRequestInstagram**](FreeToolScoreSocialAuditRequestInstagram.md) |  | [optional] |
| **mastodon** | [**FreeToolScoreSocialAuditRequestInstagram**](FreeToolScoreSocialAuditRequestInstagram.md) |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolScoreSocialAuditRequest.new(
  target_posts_per_week: null,
  instagram: null,
  facebook: null,
  linkedin: null,
  x: null,
  tiktok: null,
  youtube: null,
  pinterest: null,
  threads: null,
  bluesky: null,
  mastodon: null
)
```

