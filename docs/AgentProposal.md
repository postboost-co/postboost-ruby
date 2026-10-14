# PostBoost::AgentProposal

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **uuid** | **String** |  |  |
| **run_uuid** | **String** |  | [optional] |
| **post_uuid** | **String** |  | [optional] |
| **account_id** | **Integer** |  | [optional] |
| **kind** | **String** | &#x60;hold_post&#x60; moves the post back to draft; &#x60;edit_caption&#x60; replaces one caption; &#x60;retry_account&#x60; publishes one failed account again; &#x60;reconnect_account&#x60; asks to reconnect the account first.  |  |
| **severity** | **String** |  |  |
| **reason** | **String** |  |  |
| **payload** | **Hash&lt;String, Object&gt;** | The proposed change. &#x60;hold_post&#x60;: &#x60;reasons[]&#x60; (&#x60;code&#x60;, &#x60;account_id&#x60;, &#x60;message&#x60;, &#x60;severity&#x60;) and &#x60;scheduled_at&#x60;. &#x60;edit_caption&#x60;: &#x60;version_account_id&#x60; (0 &#x3D; original), &#x60;item_index&#x60;, &#x60;before&#x60;, &#x60;after&#x60;. &#x60;retry_account&#x60;: &#x60;error&#x60; (up to 300 characters) and, for a shortened caption, &#x60;source_account_id&#x60; (the version it was taken from, 0 &#x3D; original), &#x60;item_index&#x60;, &#x60;before&#x60;, &#x60;after&#x60;. &#x60;reconnect_account&#x60;: &#x60;error&#x60;, &#x60;reconnect_url&#x60;. All carry &#x60;post_updated_at&#x60;.  |  |
| **status** | **String** |  |  |
| **decided_at** | **Time** |  | [optional] |
| **applied_at** | **Time** |  | [optional] |
| **note** | **String** |  | [optional] |
| **error** | **String** | Why a proposal went stale or failed. | [optional] |
| **created_at** | **Time** |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::AgentProposal.new(
  uuid: null,
  run_uuid: null,
  post_uuid: null,
  account_id: null,
  kind: null,
  severity: null,
  reason: null,
  payload: null,
  status: null,
  decided_at: null,
  applied_at: null,
  note: null,
  error: null,
  created_at: null
)
```

