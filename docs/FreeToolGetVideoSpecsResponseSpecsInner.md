# PostBoost::FreeToolGetVideoSpecsResponseSpecsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **network** | **String** | Network name. | [optional] |
| **network_key** | **String** | Key for &#x60;network&#x60;. | [optional] |
| **placement** | **String** | Placement; &#x60;(app)&#x60; and &#x60;(publishing API)&#x60; rows differ where the network says so. | [optional] |
| **placement_key** | **String** | Key for &#x60;placement&#x60;. | [optional] |
| **ratio** | **String** | Aspect ratios as the source states them. | [optional] |
| **resolution** | **String** | Resolution, frame rate and codec notes. | [optional] |
| **length** | **String** | Length limits. | [optional] |
| **max_size** | **String** | File size limit. | [optional] |
| **formats** | **String** | Container and codec formats. | [optional] |
| **safe_zone** | **String** | Text safe zone, only where the network publishes one. | [optional] |
| **basis** | **String** | &#x60;official&#x60; when the network itself states it, else how it was found. | [optional] |
| **sources** | **Array&lt;String&gt;** | URLs of the sources. | [optional] |
| **limits** | [**FreeToolGetVideoSpecsResponseSpecsInnerLimits**](FreeToolGetVideoSpecsResponseSpecsInnerLimits.md) |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolGetVideoSpecsResponseSpecsInner.new(
  network: null,
  network_key: null,
  placement: null,
  placement_key: null,
  ratio: null,
  resolution: null,
  length: null,
  max_size: null,
  formats: null,
  safe_zone: null,
  basis: null,
  sources: null,
  limits: null
)
```

