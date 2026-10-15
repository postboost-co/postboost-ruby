# PostBoost::FreeToolCalculateCropResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **crop** | [**FreeToolCalculateCropResponseCrop**](FreeToolCalculateCropResponseCrop.md) |  | [optional] |
| **output** | [**FreeToolCalculateCropResponseOutput**](FreeToolCalculateCropResponseOutput.md) |  | [optional] |
| **image** | [**FreeToolCalculateCropResponseImage**](FreeToolCalculateCropResponseImage.md) |  | [optional] |
| **scale** | **Float** | Output pixels per source pixel, 4 decimals. | [optional] |
| **upscaled** | **Boolean** | True when the source is enlarged (scale above 1), which can look soft. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolCalculateCropResponse.new(
  crop: null,
  output: null,
  image: null,
  scale: null,
  upscaled: null
)
```

