# PostBoost::AgentRun

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **uuid** | **String** |  |  |
| **agent_uuid** | **String** |  |  |
| **agent_type** | **String** |  |  |
| **trigger** | **String** |  |  |
| **status** | **String** |  |  |
| **started_at** | **Time** |  | [optional] |
| **finished_at** | **Time** |  | [optional] |
| **items_checked** | **Integer** |  |  |
| **proposals_created** | **Integer** |  |  |
| **credits_used** | **Integer** | AI credits this run used. |  |
| **summary** | **String** |  | [optional] |
| **error** | **String** |  | [optional] |
| **created_at** | **Time** |  | [optional] |
| **proposals** | [**Array&lt;AgentProposal&gt;**](AgentProposal.md) | Only on &#x60;GET /agent-runs/{runUuid}&#x60;. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::AgentRun.new(
  uuid: null,
  agent_uuid: null,
  agent_type: null,
  trigger: null,
  status: null,
  started_at: null,
  finished_at: null,
  items_checked: null,
  proposals_created: null,
  credits_used: null,
  summary: null,
  error: null,
  created_at: null,
  proposals: null
)
```

