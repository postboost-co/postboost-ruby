# PostBoost::FreeToolCalculateAspectRatioResponseMatchesInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **network** | **String** | Network key from getImageSizes (&#x60;network_key&#x60;). | [optional] |
| **format** | **String** | Format key from getImageSizes (&#x60;format_key&#x60;). | [optional] |
| **width** | **Integer** |  | [optional] |
| **height** | **Integer** |  | [optional] |
| **ratio** | **String** |  | [optional] |
| **exact** | **Boolean** | False when no preset has the same ratio and these are the nearest. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolCalculateAspectRatioResponseMatchesInner.new(
  network: null,
  format: null,
  width: null,
  height: null,
  ratio: null,
  exact: null
)
```

