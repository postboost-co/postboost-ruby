# PostBoost::FreeToolCheckLinkPreviewResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **final_url** | **String** | The URL after redirects. | [optional] |
| **status** | **Integer** | HTTP status of the final response. | [optional] |
| **redirects** | [**Array&lt;FreeToolCheckLinkPreviewResponseRedirectsInner&gt;**](FreeToolCheckLinkPreviewResponseRedirectsInner.md) |  | [optional] |
| **content_type** | **String** |  | [optional] |
| **tags** | [**FreeToolCheckLinkPreviewResponseTags**](FreeToolCheckLinkPreviewResponseTags.md) |  | [optional] |
| **image** | [**FreeToolCheckLinkPreviewResponseImage**](FreeToolCheckLinkPreviewResponseImage.md) |  | [optional] |
| **previews** | [**Hash&lt;String, FreeToolCheckLinkPreviewResponsePreviewsValue&gt;**](FreeToolCheckLinkPreviewResponsePreviewsValue.md) | The card each network would show. | [optional] |
| **warnings** | **Array&lt;String&gt;** |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolCheckLinkPreviewResponse.new(
  final_url: null,
  status: null,
  redirects: null,
  content_type: null,
  tags: null,
  image: null,
  previews: null,
  warnings: null
)
```

