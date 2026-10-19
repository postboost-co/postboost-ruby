# PostBoost::FreeToolPickSocialMediaToolResponseResultsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **slug** | **String** |  | [optional] |
| **name** | **String** |  | [optional] |
| **score** | **Integer** | How many of your needs the tool meets. | [optional] |
| **matched** | **Array&lt;String&gt;** |  | [optional] |
| **missing** | **Array&lt;String&gt;** |  | [optional] |
| **unknown** | **Array&lt;String&gt;** | Needs the tool&#39;s public docs did not show either way (\&quot;not documented\&quot;). | [optional] |
| **compare_url** | **String** | Path of the full PostBoost comparison page; null for PostBoost. | [optional] |
| **checked_at** | **Date** | When the tool&#39;s data was last checked. | [optional] |
| **pick_if** | **String** | When this tool is the better choice; null for PostBoost. | [optional] |
| **postboost_if** | **String** | When PostBoost is the better choice; null for PostBoost. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolPickSocialMediaToolResponseResultsInner.new(
  slug: null,
  name: null,
  score: null,
  matched: null,
  missing: null,
  unknown: null,
  compare_url: null,
  checked_at: null,
  pick_if: null,
  postboost_if: null
)
```

