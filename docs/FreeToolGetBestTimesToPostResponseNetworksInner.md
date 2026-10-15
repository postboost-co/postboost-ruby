# PostBoost::FreeToolGetBestTimesToPostResponseNetworksInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **network** | **String** |  | [optional] |
| **network_key** | **String** | Key for &#x60;network&#x60;. | [optional] |
| **columns** | **Array&lt;String&gt;** | One column per study. | [optional] |
| **rows** | **Array&lt;Array&lt;String&gt;&gt;** | Weekday (or &#x60;Best&#x60;), then one cell per study, in the audience&#39;s local time. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolGetBestTimesToPostResponseNetworksInner.new(
  network: null,
  network_key: null,
  columns: null,
  rows: null
)
```

