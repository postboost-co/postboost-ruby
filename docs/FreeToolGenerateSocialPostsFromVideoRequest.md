# PostBoost::FreeToolGenerateSocialPostsFromVideoRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **text** | **String** | The captions of your video: an .srt, .vtt or .sbv file&#39;s text, or the text of YouTube&#39;s \&quot;Show transcript\&quot; panel. Timestamps, cue numbers and sound tags like [Music] are removed; 100 to 24,000 characters must remain. |  |
| **video_url** | **String** | The video&#39;s YouTube link (watch, youtu.be, Shorts or live). Each output links it once, the X thread in its last post; without it the posts have no link. | [optional] |
| **title** | **String** | The video&#39;s title, as context for the posts. | [optional] |
| **outputs** | **Array&lt;String&gt;** | What to write, 1 to 4 different keys. | [optional] |
| **tone** | **String** |  | [optional][default to &#39;friendly&#39;] |
| **workspace** | **String** | UUID of the workspace whose AI credits pay for the call. Default: your active workspace (a scoped API key: its own workspace). | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolGenerateSocialPostsFromVideoRequest.new(
  text: null,
  video_url: null,
  title: null,
  outputs: null,
  tone: null,
  workspace: null
)
```

