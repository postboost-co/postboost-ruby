# PostBoost::PostVersion

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | Use &#x60;0&#x60; for the original/default version. |  |
| **is_original** | **Boolean** | Must be &#x60;true&#x60; for the first version. |  |
| **synced_with** | **Integer** | Account ID of the version this version follows (&#x60;0&#x60; &#x3D; the original), or null when it is edited independently. Ignored on the original version. | [optional] |
| **content** | [**Array&lt;PostContent&gt;**](PostContent.md) | Ordered content items. Item 0 is the post. Item 1 is the first comment on Facebook Page, Instagram and LinkedIn, or the next thread post on X, Threads, Bluesky, Mastodon and Pixelfed. See &#x60;PostContent&#x60;.  |  |
| **options** | [**PostVersionOptions**](PostVersionOptions.md) |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::PostVersion.new(
  account_id: null,
  is_original: null,
  synced_with: null,
  content: null,
  options: null
)
```

