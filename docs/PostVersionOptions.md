# PostBoost::PostVersionOptions

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **tiktok** | [**PostOptionsTikTok**](PostOptionsTikTok.md) |  | [optional] |
| **youtube** | [**PostOptionsYoutube**](PostOptionsYoutube.md) |  | [optional] |
| **instagram** | [**PostOptionsInstagram**](PostOptionsInstagram.md) |  | [optional] |
| **instagram_standalone** | [**PostOptionsInstagram**](PostOptionsInstagram.md) |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::PostVersionOptions.new(
  tiktok: null,
  youtube: null,
  instagram: null,
  instagram_standalone: null
)
```

