# PostBoost::PostOptionsTikTok

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **privacy_level** | **Hash&lt;String, String&gt;** |  | [optional] |
| **is_aigc** | **Hash&lt;String, Boolean&gt;** | TikTok&#39;s \&quot;AI-generated content\&quot; label. | [optional] |
| **allow_comments** | **Hash&lt;String, Boolean&gt;** |  | [optional] |
| **allow_duet** | **Hash&lt;String, Boolean&gt;** |  | [optional] |
| **allow_stitch** | **Hash&lt;String, Boolean&gt;** |  | [optional] |
| **auto_add_music** | **Hash&lt;String, Boolean&gt;** |  | [optional] |
| **content_disclosure** | **Hash&lt;String, Boolean&gt;** | Discloses branded or promotional content; then set &#x60;brand_organic_toggle&#x60; and/or &#x60;brand_content_toggle&#x60;. | [optional] |
| **brand_organic_toggle** | **Hash&lt;String, Boolean&gt;** |  | [optional] |
| **brand_content_toggle** | **Hash&lt;String, Boolean&gt;** |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::PostOptionsTikTok.new(
  privacy_level: {account-12&#x3D;PUBLIC_TO_EVERYONE},
  is_aigc: {account-12&#x3D;true},
  allow_comments: null,
  allow_duet: null,
  allow_stitch: null,
  auto_add_music: null,
  content_disclosure: null,
  brand_organic_toggle: null,
  brand_content_toggle: null
)
```

