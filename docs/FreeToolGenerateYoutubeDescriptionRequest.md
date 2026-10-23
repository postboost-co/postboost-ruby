# PostBoost::FreeToolGenerateYoutubeDescriptionRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **text** | **String** | What the video is about: a summary or the main points. |  |
| **keywords** | **String** | Optional search keywords to use naturally, comma separated. | [optional] |
| **chapters** | **Boolean** | Add a chapters block after the first paragraph. | [optional][default to false] |
| **chapter_lines** | **Array&lt;String&gt;** | Your chapters as &#x60;m:ss Title&#x60; lines, the first at 0:00. Used verbatim when &#x60;chapters&#x60; is true; without them the block has fill-in placeholders. Timestamps are never generated. | [optional] |
| **cta** | **String** | The closing call to action: subscribe, link (a [link] placeholder) or none. | [optional][default to &#39;subscribe&#39;] |
| **workspace** | **String** | UUID of the workspace whose AI credits pay for the call. Default: your active workspace (a scoped API key: its own workspace). | [optional] |
| **transcript** | **String** | Optional: your video&#39;s captions (.srt, .vtt, .sbv or the Show transcript text) as context; timestamps are removed and the first 6,000 characters are used. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolGenerateYoutubeDescriptionRequest.new(
  text: null,
  keywords: null,
  chapters: null,
  chapter_lines: null,
  cta: null,
  workspace: null,
  transcript: null
)
```

