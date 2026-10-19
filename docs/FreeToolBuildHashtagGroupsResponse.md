# PostBoost::FreeToolBuildHashtagGroupsResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **hashtags** | **Array&lt;String&gt;** | Clean hashtags in input order, duplicates removed. | [optional] |
| **removed** | [**Array&lt;FreeToolBuildHashtagGroupsResponseRemovedInner&gt;**](FreeToolBuildHashtagGroupsResponseRemovedInner.md) | Entries that were dropped, with the reason. | [optional] |
| **cap** | **Integer** | Hashtags PostBoost allows per post on the network; null &#x3D; no hard limit. | [optional] |
| **group_size** | **Integer** | Hashtags per group that was used. | [optional] |
| **groups** | [**Array&lt;FreeToolBuildHashtagGroupsResponseGroupsInner&gt;**](FreeToolBuildHashtagGroupsResponseGroupsInner.md) |  | [optional] |
| **over_cap** | **Boolean** | A group holds more hashtags than the cap. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolBuildHashtagGroupsResponse.new(
  hashtags: null,
  removed: null,
  cap: null,
  group_size: null,
  groups: null,
  over_cap: null
)
```

