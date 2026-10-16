# PostBoost::Account

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** |  |  |
| **uuid** | **String** |  |  |
| **name** | **String** |  |  |
| **username** | **String** |  |  |
| **image** | **String** |  | [optional] |
| **provider** | **String** | Network key. Known values: &#x60;twitter&#x60;, &#x60;facebook_page&#x60;, &#x60;instagram&#x60;, &#x60;instagram_standalone&#x60;, &#x60;threads&#x60;, &#x60;linkedin&#x60;, &#x60;linkedin_page&#x60;, &#x60;tiktok&#x60;, &#x60;youtube&#x60;, &#x60;pinterest&#x60;, &#x60;gbp&#x60;, &#x60;bluesky&#x60;, &#x60;mastodon&#x60;, &#x60;pixelfed&#x60;, &#x60;telegram&#x60;, &#x60;discord&#x60;, &#x60;slack&#x60;. New networks add new keys, so treat unknown values as valid.  |  |
| **data** | **Object** | Provider-specific metadata. |  |
| **authorized** | **Boolean** |  |  |
| **profile_url** | **String** | Public URL of the account&#39;s profile on the network, when known. | [optional] |
| **publish_status** | **String** | Only present when the account is embedded in a post. Publishing state of this account for the post. | [optional] |
| **published_parts** | **Integer** | Only present when the account is embedded in a post. How many parts (for example thread items or a first comment) are live on the network. | [optional] |
| **external_url** | **String** | Only present when the account is embedded in a post. URL of the published post on the network, null until it is live. | [optional] |
| **provider_post_id** | **String** | Only present when the account is embedded in a post. The network&#39;s own ID of the published post (for example a LinkedIn share URN or a tweet ID), null until it is live. | [optional] |
| **errors** | [**Array&lt;AccountErrorsInner&gt;**](AccountErrorsInner.md) | Only present when the account is embedded in a post. Why publishing to this account failed. A raw network error is stored as two entries: a readable line (&#x60;\&quot;&lt;Network&gt;: &lt;message&gt; (code &lt;code&gt;)\&quot;&#x60;) and an object &#x60;{platform, code, message, raw}&#x60; with the network&#39;s original response in &#x60;raw&#x60;. Other failures are a single readable string.  | [optional] |
| **created_at** | **String** | UTC, formatted &#x60;Y-m-d H:i:s&#x60;. |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::Account.new(
  id: null,
  uuid: null,
  name: My Instagram,
  username: myhandle,
  image: null,
  provider: instagram,
  data: null,
  authorized: null,
  profile_url: null,
  publish_status: null,
  published_parts: null,
  external_url: null,
  provider_post_id: null,
  errors: null,
  created_at: 2026-10-11 09:30:00
)
```

