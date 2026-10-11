# PostBoost::AccountAnalytics

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account** | [**Account**](Account.md) |  |  |
| **type** | **String** | The analytics tab returned. |  |
| **tabs** | **Array&lt;String&gt;** | Tabs this account supports; any of them can be passed as &#x60;type&#x60;. |  |
| **period** | [**AnalyticsPeriod**](AnalyticsPeriod.md) |  |  |
| **initial_sync** | [**AccountAnalyticsInitialSync**](AccountAnalyticsInitialSync.md) |  |  |
| **data** | **Hash&lt;String, Object&gt;** | Provider- and tab-specific metrics. Chart series are lists of &#x60;{date, value}&#x60; points. |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::AccountAnalytics.new(
  account: null,
  type: null,
  tabs: null,
  period: null,
  initial_sync: null,
  data: null
)
```

