# PostBoost::RssFeedInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **url** | **String** | Public http(s) URL of an RSS 2.0 or Atom feed. |  |
| **name** | **String** |  | [optional] |
| **account_ids** | **Array&lt;Integer&gt;** |  |  |
| **mode** | **String** |  | [optional][default to &#39;draft&#39;] |
| **template** | **String** | Post text. Placeholders: &#x60;{title}&#x60;, &#x60;{link}&#x60;, &#x60;{summary}&#x60; (up to 280 characters). Default &#x60;{title}&#x60; + blank line + &#x60;{link}&#x60;. | [optional] |
| **max_items_per_run** | **Integer** |  | [optional][default to 3] |
| **active** | **Boolean** |  | [optional][default to true] |

## Example

```ruby
require 'postboost'

instance = PostBoost::RssFeedInput.new(
  url: null,
  name: null,
  account_ids: null,
  mode: null,
  template: null,
  max_items_per_run: null,
  active: null
)
```

