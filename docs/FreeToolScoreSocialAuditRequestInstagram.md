# PostBoost::FreeToolScoreSocialAuditRequestInstagram

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **profile** | **String** | Profile photo, name and cover image match your brand. | [optional][default to &#39;no&#39;] |
| **bio** | **String** | Your bio says who you help and how, and has a link. | [optional][default to &#39;no&#39;] |
| **link_tracking** | **String** | The bio link carries UTM tags. | [optional][default to &#39;no&#39;] |
| **frequency** | **String** | You publish at least N posts a week, your own target. | [optional][default to &#39;no&#39;] |
| **replies** | **String** | You reply to comments and messages within 24 hours. | [optional][default to &#39;no&#39;] |
| **native_formats** | **String** | You use the formats the network is built for, such as short video, carousels or documents. | [optional][default to &#39;no&#39;] |
| **pinned** | **String** | Your pinned or featured post is current. | [optional][default to &#39;no&#39;] |
| **engagement_rate** | **String** | You check your engagement rate every month. | [optional][default to &#39;no&#39;] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolScoreSocialAuditRequestInstagram.new(
  profile: null,
  bio: null,
  link_tracking: null,
  frequency: null,
  replies: null,
  native_formats: null,
  pinned: null,
  engagement_rate: null
)
```

