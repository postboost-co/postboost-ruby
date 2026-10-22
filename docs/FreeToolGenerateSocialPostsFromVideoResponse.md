# PostBoost::FreeToolGenerateSocialPostsFromVideoResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **outputs** | [**FreeToolGenerateSocialPostsFromVideoResponseOutputs**](FreeToolGenerateSocialPostsFromVideoResponseOutputs.md) |  | [optional] |
| **outputs_skipped** | **Array&lt;String&gt;** | Requested outputs that came back empty: generate again to get them. | [optional] |
| **warnings** | **Array&lt;String&gt;** | What to know before posting, in plain words. | [optional] |
| **video_url** | **String** | The normalised video link the posts use, or null. | [optional] |
| **cleaned_chars** | **Integer** | Characters of caption text left after cleaning; the model read these. | [optional] |
| **removed_timestamps** | **Boolean** | True when timestamps, cue numbers, tags or repeated caption lines were removed. | [optional] |
| **credits_spent** | **Integer** | AI credits this call took from the workspace: 1, or 0 for a cached result. | [optional] |
| **cached** | **Boolean** | True when the same request was answered before (free). | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolGenerateSocialPostsFromVideoResponse.new(
  outputs: null,
  outputs_skipped: null,
  warnings: null,
  video_url: null,
  cleaned_chars: null,
  removed_timestamps: null,
  credits_spent: null,
  cached: null
)
```

