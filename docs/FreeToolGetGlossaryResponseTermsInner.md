# PostBoost::FreeToolGetGlossaryResponseTermsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **term** | **String** | The term. | [optional] |
| **slug** | **String** | Stable key of the term, also its anchor on the page. | [optional] |
| **category** | **String** | Category. | [optional] |
| **definition** | **String** | Plain-language definition in one to three sentences. | [optional] |
| **networks** | **Array&lt;String&gt;** | Networks the term is specific to (provider keys); empty when it applies to all. | [optional] |
| **related** | **Array&lt;String&gt;** | Slugs of related terms. | [optional] |
| **url** | **String** | The term on the glossary page. | [optional] |
| **learn_url** | **String** | A PostBoost guide that goes deeper, or null. | [optional] |
| **tool_url** | **String** | A free tool for the job, or null. | [optional] |
| **feature_url** | **String** | The PostBoost feature page, or null. | [optional] |
| **source** | **String** | Where a platform rule or number in the definition comes from, or null. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolGetGlossaryResponseTermsInner.new(
  term: null,
  slug: null,
  category: null,
  definition: null,
  networks: null,
  related: null,
  url: null,
  learn_url: null,
  tool_url: null,
  feature_url: null,
  source: null
)
```

