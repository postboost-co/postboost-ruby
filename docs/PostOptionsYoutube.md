# PostBoost::PostOptionsYoutube

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **title** | **String** |  | [optional] |
| **status** | **String** |  | [optional][default to &#39;public&#39;] |
| **made_for_kids** | **Boolean** |  | [optional][default to false] |
| **contains_synthetic_media** | **Boolean** | YouTube&#39;s \&quot;altered or synthetic content\&quot; disclosure. Set by &#x60;ai_generated&#x60;. | [optional][default to false] |

## Example

```ruby
require 'postboost'

instance = PostBoost::PostOptionsYoutube.new(
  title: null,
  status: null,
  made_for_kids: null,
  contains_synthetic_media: null
)
```

