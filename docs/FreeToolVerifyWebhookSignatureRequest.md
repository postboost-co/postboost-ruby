# PostBoost::FreeToolVerifyWebhookSignatureRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **body** | **String** | The raw request body exactly as received (up to 64 KB). Use a test payload, not production data. |  |
| **secret** | **String** | The webhook secret. Use a test secret: never send a production secret to any third-party service. |  |
| **signature** | **String** | The received signature header value, e.g. X-Signature. |  |
| **algorithm** | **String** |  | [optional][default to &#39;sha256&#39;] |
| **encoding** | **String** |  | [optional][default to &#39;hex&#39;] |
| **prefix** | **String** | A prefix the sender puts before the signature, e.g. \&quot;sha256&#x3D;\&quot; (GitHub). | [optional][default to &#39;&#39;] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolVerifyWebhookSignatureRequest.new(
  body: null,
  secret: null,
  signature: null,
  algorithm: null,
  encoding: null,
  prefix: null
)
```

