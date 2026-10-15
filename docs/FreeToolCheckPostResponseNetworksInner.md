# PostBoost::FreeToolCheckPostResponseNetworksInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **key** | **String** |  | [optional] |
| **label** | **String** |  | [optional] |
| **ok** | **Boolean** | False when an error would stop the post from publishing. | [optional] |
| **count** | **Integer** | Characters as this network counts them. | [optional] |
| **limit** | **Integer** |  | [optional] |
| **errors** | [**Array&lt;FreeToolCheckPostResponseNetworksInnerErrorsInner&gt;**](FreeToolCheckPostResponseNetworksInnerErrorsInner.md) | Codes: too_long, too_many_hashtags, media_required, too_many_media, media_type, video_too_long, video_too_short. | [optional] |
| **warnings** | [**Array&lt;FreeToolCheckPostResponseNetworksInnerErrorsInner&gt;**](FreeToolCheckPostResponseNetworksInnerErrorsInner.md) | Codes: cut_by_fold, link_not_clickable. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolCheckPostResponseNetworksInner.new(
  key: null,
  label: null,
  ok: null,
  count: null,
  limit: null,
  errors: null,
  warnings: null
)
```

