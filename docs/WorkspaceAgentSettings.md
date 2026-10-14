# PostBoost::WorkspaceAgentSettings

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **horizon_hours** | **Integer** | Check posts scheduled within this many hours. | [optional][default to 24] |
| **check_links** | **Boolean** | Flag links in captions that answer an HTTP error. | [optional][default to true] |
| **banned_phrases** | **Array&lt;String&gt;** | Phrases to propose removing from captions. | [optional] |
| **ai_review** | **Boolean** | Ask AI to review captions (one AI credit per reviewed post). | [optional][default to false] |
| **max_ai_reviews_per_run** | **Integer** |  | [optional][default to 10] |
| **lookback_hours** | **Integer** | Look at posts that failed within this many hours. | [optional][default to 24] |

## Example

```ruby
require 'postboost'

instance = PostBoost::WorkspaceAgentSettings.new(
  horizon_hours: null,
  check_links: null,
  banned_phrases: null,
  ai_review: null,
  max_ai_reviews_per_run: null,
  lookback_hours: null
)
```

