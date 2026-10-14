# PostBoost::AgentsApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**approve_agent_proposal**](AgentsApi.md#approve_agent_proposal) | **POST** /{workspaceUuid}/agent-proposals/{proposalUuid}/approve | Approve and apply an agent proposal |
| [**create_agent**](AgentsApi.md#create_agent) | **POST** /{workspaceUuid}/agents | Switch on a background agent |
| [**delete_agent**](AgentsApi.md#delete_agent) | **DELETE** /{workspaceUuid}/agents/{agentUuid} | Delete a background agent |
| [**get_agent_run**](AgentsApi.md#get_agent_run) | **GET** /{workspaceUuid}/agent-runs/{runUuid} | Get an agent run with its proposals |
| [**list_agent_proposals**](AgentsApi.md#list_agent_proposals) | **GET** /{workspaceUuid}/agent-proposals | List agent proposals (approval queue) |
| [**list_agent_runs**](AgentsApi.md#list_agent_runs) | **GET** /{workspaceUuid}/agents/{agentUuid}/runs | Run history of an agent |
| [**list_agents**](AgentsApi.md#list_agents) | **GET** /{workspaceUuid}/agents | List background agents |
| [**reject_agent_proposal**](AgentsApi.md#reject_agent_proposal) | **POST** /{workspaceUuid}/agent-proposals/{proposalUuid}/reject | Reject an agent proposal |
| [**run_agent**](AgentsApi.md#run_agent) | **POST** /{workspaceUuid}/agents/{agentUuid}/run | Run a background agent now |
| [**update_agent**](AgentsApi.md#update_agent) | **PUT** /{workspaceUuid}/agents/{agentUuid} | Update a background agent |


## approve_agent_proposal

> <ApproveAgentProposal200Response> approve_agent_proposal(workspace_uuid, proposal_uuid, opts)

Approve and apply an agent proposal

Applies the proposal at once: `hold_post` moves the post back to draft, `edit_caption` replaces the caption, `retry_account` saves the shortened caption (if any) on that account's version and publishes that account again, `reconnect_account` only records the decision. When the post was edited, deleted or left the schedule since the proposal was made (for `retry_account`: the account is no longer failed, the post is publishing, or the plan does not allow scheduling), nothing changes and the proposal becomes `stale`. Admins and members only. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::AgentsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
proposal_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
opts = {
  agent_proposal_decision: PostBoost::AgentProposalDecision.new # AgentProposalDecision | 
}

begin
  # Approve and apply an agent proposal
  result = api_instance.approve_agent_proposal(workspace_uuid, proposal_uuid, opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AgentsApi->approve_agent_proposal: #{e}"
end
```

#### Using the approve_agent_proposal_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ApproveAgentProposal200Response>, Integer, Hash)> approve_agent_proposal_with_http_info(workspace_uuid, proposal_uuid, opts)

```ruby
begin
  # Approve and apply an agent proposal
  data, status_code, headers = api_instance.approve_agent_proposal_with_http_info(workspace_uuid, proposal_uuid, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ApproveAgentProposal200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling AgentsApi->approve_agent_proposal_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **proposal_uuid** | **String** |  |  |
| **agent_proposal_decision** | [**AgentProposalDecision**](AgentProposalDecision.md) |  | [optional] |

### Return type

[**ApproveAgentProposal200Response**](ApproveAgentProposal200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## create_agent

> <CreateAgent201Response> create_agent(workspace_uuid, workspace_agent_input)

Switch on a background agent

Creates an agent (one per type per workspace). It first runs within five minutes, then on its `schedule`. **Pre-publish checker** looks at posts scheduled in the next `horizon_hours` and proposes holding (back to draft) posts that would fail: disconnected accounts, network requirements, daily caps, the X allowance and links that answer an error. It proposes caption edits that drop `banned_phrases`. With `ai_review: true` it also asks AI to review up to `max_ai_reviews_per_run` posts per run (one AI credit each). **Failed-post fixer** looks at posts that failed on an account in the last `lookback_hours` and proposes, per post and account, `reconnect_account` (the account's token expired), or `retry_account`, with a caption trimmed to the network limit when the text is over it. One open proposal per post and account. It uses no AI. Admins and members only. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::AgentsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
workspace_agent_input = PostBoost::WorkspaceAgentInput.new({type: 'pre_publish_checker'}) # WorkspaceAgentInput | 

begin
  # Switch on a background agent
  result = api_instance.create_agent(workspace_uuid, workspace_agent_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AgentsApi->create_agent: #{e}"
end
```

#### Using the create_agent_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateAgent201Response>, Integer, Hash)> create_agent_with_http_info(workspace_uuid, workspace_agent_input)

```ruby
begin
  # Switch on a background agent
  data, status_code, headers = api_instance.create_agent_with_http_info(workspace_uuid, workspace_agent_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateAgent201Response>
rescue PostBoost::ApiError => e
  puts "Error when calling AgentsApi->create_agent_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **workspace_agent_input** | [**WorkspaceAgentInput**](WorkspaceAgentInput.md) |  |  |

### Return type

[**CreateAgent201Response**](CreateAgent201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_agent

> <DeleteAgent200Response> delete_agent(workspace_uuid, agent_uuid)

Delete a background agent

Removes the agent. Its run history and proposals stay. Admins and members only.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::AgentsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
agent_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  # Delete a background agent
  result = api_instance.delete_agent(workspace_uuid, agent_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AgentsApi->delete_agent: #{e}"
end
```

#### Using the delete_agent_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DeleteAgent200Response>, Integer, Hash)> delete_agent_with_http_info(workspace_uuid, agent_uuid)

```ruby
begin
  # Delete a background agent
  data, status_code, headers = api_instance.delete_agent_with_http_info(workspace_uuid, agent_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DeleteAgent200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling AgentsApi->delete_agent_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **agent_uuid** | **String** |  |  |

### Return type

[**DeleteAgent200Response**](DeleteAgent200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_agent_run

> <RunAgent202Response> get_agent_run(workspace_uuid, run_uuid)

Get an agent run with its proposals

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::AgentsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
run_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  # Get an agent run with its proposals
  result = api_instance.get_agent_run(workspace_uuid, run_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AgentsApi->get_agent_run: #{e}"
end
```

#### Using the get_agent_run_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<RunAgent202Response>, Integer, Hash)> get_agent_run_with_http_info(workspace_uuid, run_uuid)

```ruby
begin
  # Get an agent run with its proposals
  data, status_code, headers = api_instance.get_agent_run_with_http_info(workspace_uuid, run_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <RunAgent202Response>
rescue PostBoost::ApiError => e
  puts "Error when calling AgentsApi->get_agent_run_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **run_uuid** | **String** |  |  |

### Return type

[**RunAgent202Response**](RunAgent202Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_agent_proposals

> <ListAgentProposals200Response> list_agent_proposals(workspace_uuid, opts)

List agent proposals (approval queue)

Proposals of all agents in the workspace, newest first. Defaults to `pending`.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::AgentsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
opts = {
  status: 'pending', # String | 
  per_page: 56, # Integer | 
  page: 56 # Integer | 
}

begin
  # List agent proposals (approval queue)
  result = api_instance.list_agent_proposals(workspace_uuid, opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AgentsApi->list_agent_proposals: #{e}"
end
```

#### Using the list_agent_proposals_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListAgentProposals200Response>, Integer, Hash)> list_agent_proposals_with_http_info(workspace_uuid, opts)

```ruby
begin
  # List agent proposals (approval queue)
  data, status_code, headers = api_instance.list_agent_proposals_with_http_info(workspace_uuid, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListAgentProposals200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling AgentsApi->list_agent_proposals_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **status** | **String** |  | [optional][default to &#39;pending&#39;] |
| **per_page** | **Integer** |  | [optional][default to 20] |
| **page** | **Integer** |  | [optional] |

### Return type

[**ListAgentProposals200Response**](ListAgentProposals200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_agent_runs

> <ListAgentRuns200Response> list_agent_runs(workspace_uuid, agent_uuid, opts)

Run history of an agent

Runs of the agent, newest first, with what each checked and proposed and the AI credits it used.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::AgentsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
agent_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
opts = {
  per_page: 56, # Integer | 
  page: 56 # Integer | 
}

begin
  # Run history of an agent
  result = api_instance.list_agent_runs(workspace_uuid, agent_uuid, opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AgentsApi->list_agent_runs: #{e}"
end
```

#### Using the list_agent_runs_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListAgentRuns200Response>, Integer, Hash)> list_agent_runs_with_http_info(workspace_uuid, agent_uuid, opts)

```ruby
begin
  # Run history of an agent
  data, status_code, headers = api_instance.list_agent_runs_with_http_info(workspace_uuid, agent_uuid, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListAgentRuns200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling AgentsApi->list_agent_runs_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **agent_uuid** | **String** |  |  |
| **per_page** | **Integer** |  | [optional][default to 20] |
| **page** | **Integer** |  | [optional] |

### Return type

[**ListAgentRuns200Response**](ListAgentRuns200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_agents

> <ListAgents200Response> list_agents(workspace_uuid)

List background agents

Background agents switched on for the workspace. Agents run on a schedule, record every run and never change a post themselves: each change is a proposal that a workspace admin or member approves. Available types: `pre_publish_checker`, `failed_post_fixer`. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::AgentsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.

begin
  # List background agents
  result = api_instance.list_agents(workspace_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AgentsApi->list_agents: #{e}"
end
```

#### Using the list_agents_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListAgents200Response>, Integer, Hash)> list_agents_with_http_info(workspace_uuid)

```ruby
begin
  # List background agents
  data, status_code, headers = api_instance.list_agents_with_http_info(workspace_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListAgents200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling AgentsApi->list_agents_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |

### Return type

[**ListAgents200Response**](ListAgents200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## reject_agent_proposal

> <ApproveAgentProposal200Response> reject_agent_proposal(workspace_uuid, proposal_uuid, opts)

Reject an agent proposal

Records the rejection (and optional note); nothing changes on the post. Admins and members only.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::AgentsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
proposal_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
opts = {
  agent_proposal_decision: PostBoost::AgentProposalDecision.new # AgentProposalDecision | 
}

begin
  # Reject an agent proposal
  result = api_instance.reject_agent_proposal(workspace_uuid, proposal_uuid, opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AgentsApi->reject_agent_proposal: #{e}"
end
```

#### Using the reject_agent_proposal_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ApproveAgentProposal200Response>, Integer, Hash)> reject_agent_proposal_with_http_info(workspace_uuid, proposal_uuid, opts)

```ruby
begin
  # Reject an agent proposal
  data, status_code, headers = api_instance.reject_agent_proposal_with_http_info(workspace_uuid, proposal_uuid, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ApproveAgentProposal200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling AgentsApi->reject_agent_proposal_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **proposal_uuid** | **String** |  |  |
| **agent_proposal_decision** | [**AgentProposalDecision**](AgentProposalDecision.md) |  | [optional] |

### Return type

[**ApproveAgentProposal200Response**](ApproveAgentProposal200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## run_agent

> <RunAgent202Response> run_agent(workspace_uuid, agent_uuid)

Run a background agent now

Queues a run outside the schedule (`trigger: manual`). Six per hour. Admins and members only.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::AgentsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
agent_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  # Run a background agent now
  result = api_instance.run_agent(workspace_uuid, agent_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AgentsApi->run_agent: #{e}"
end
```

#### Using the run_agent_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<RunAgent202Response>, Integer, Hash)> run_agent_with_http_info(workspace_uuid, agent_uuid)

```ruby
begin
  # Run a background agent now
  data, status_code, headers = api_instance.run_agent_with_http_info(workspace_uuid, agent_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <RunAgent202Response>
rescue PostBoost::ApiError => e
  puts "Error when calling AgentsApi->run_agent_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **agent_uuid** | **String** |  |  |

### Return type

[**RunAgent202Response**](RunAgent202Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_agent

> <CreateAgent201Response> update_agent(workspace_uuid, agent_uuid, workspace_agent_update)

Update a background agent

Changes the name, schedule, settings or `enabled`. Settings you leave out keep their value. Admins and members only.

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::AgentsApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
agent_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
workspace_agent_update = PostBoost::WorkspaceAgentUpdate.new # WorkspaceAgentUpdate | 

begin
  # Update a background agent
  result = api_instance.update_agent(workspace_uuid, agent_uuid, workspace_agent_update)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling AgentsApi->update_agent: #{e}"
end
```

#### Using the update_agent_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateAgent201Response>, Integer, Hash)> update_agent_with_http_info(workspace_uuid, agent_uuid, workspace_agent_update)

```ruby
begin
  # Update a background agent
  data, status_code, headers = api_instance.update_agent_with_http_info(workspace_uuid, agent_uuid, workspace_agent_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateAgent201Response>
rescue PostBoost::ApiError => e
  puts "Error when calling AgentsApi->update_agent_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **agent_uuid** | **String** |  |  |
| **workspace_agent_update** | [**WorkspaceAgentUpdate**](WorkspaceAgentUpdate.md) |  |  |

### Return type

[**CreateAgent201Response**](CreateAgent201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

