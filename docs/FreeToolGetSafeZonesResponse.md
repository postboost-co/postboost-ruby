# PostBoost::FreeToolGetSafeZonesResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **platform** | **String** |  | [optional] |
| **label** | **String** | Platform name. | [optional] |
| **width** | **Integer** |  | [optional] |
| **height** | **Integer** |  | [optional] |
| **unsafe_areas** | [**Array&lt;FreeToolGetSafeZonesResponseUnsafeAreasInner&gt;**](FreeToolGetSafeZonesResponseUnsafeAreasInner.md) | Areas the app&#39;s UI usually covers, in frame pixels from the top-left corner. Edges are scaled from 1080 × 1920 and rounded to the nearest pixel (halves up), so neighbouring boxes stay edge to edge. | [optional] |
| **safe_area** | [**FreeToolGetSafeZonesResponseSafeArea**](FreeToolGetSafeZonesResponseSafeArea.md) |  | [optional] |
| **source** | [**FreeToolGetSafeZonesResponseSource**](FreeToolGetSafeZonesResponseSource.md) |  | [optional] |
| **last_verified** | **String** | Date the sources were last checked (YYYY-MM-DD). | [optional] |
| **caveat** | **String** |  | [optional] |
| **warnings** | **Array&lt;String&gt;** | Set when the frame is not 9:16, so the boxes are stretched. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolGetSafeZonesResponse.new(
  platform: null,
  label: null,
  width: null,
  height: null,
  unsafe_areas: null,
  safe_area: null,
  source: null,
  last_verified: null,
  caveat: null,
  warnings: null
)
```

