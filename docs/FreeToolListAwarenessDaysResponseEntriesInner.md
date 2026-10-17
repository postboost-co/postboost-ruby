# PostBoost::FreeToolListAwarenessDaysResponseEntriesInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | Name of the holiday or observance. | [optional] |
| **type** | **String** | Entry type. | [optional] |
| **date** | **Date** | The day, or the first day of a week or month. | [optional] |
| **_end** | **Date** | Last day of a week or month (inclusive); null for a single day. | [optional] |
| **countries** | **Array&lt;String&gt;** | Country codes, or &#x60;global&#x60;. | [optional] |
| **topics** | **Array&lt;String&gt;** | Topics. | [optional] |
| **source** | **String** | Official or organiser page the date comes from. | [optional] |
| **note** | **String** | Regional scope or a day off that differs from the date. | [optional] |
| **idea** | **String** | A one-line post idea. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolListAwarenessDaysResponseEntriesInner.new(
  name: null,
  type: null,
  date: null,
  _end: null,
  countries: null,
  topics: null,
  source: null,
  note: null,
  idea: null
)
```

