# PostBoost::InboxApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**approve_inbox_reply_draft**](InboxApi.md#approve_inbox_reply_draft) | **POST** /{workspaceUuid}/inbox/drafts/{draftId}/approve | Approve and send a reply draft |
| [**create_inbox_reply_draft**](InboxApi.md#create_inbox_reply_draft) | **POST** /{workspaceUuid}/inbox/conversations/{conversationId}/drafts | Draft a reply |
| [**delete_inbox_reply_draft**](InboxApi.md#delete_inbox_reply_draft) | **DELETE** /{workspaceUuid}/inbox/drafts/{draftId} | Withdraw a reply draft |
| [**get_inbox_conversation**](InboxApi.md#get_inbox_conversation) | **GET** /{workspaceUuid}/inbox/conversations/{conversationId} | Get an inbox conversation |
| [**get_inbox_reply_draft**](InboxApi.md#get_inbox_reply_draft) | **GET** /{workspaceUuid}/inbox/drafts/{draftId} | Get a reply draft |
| [**list_inbox_conversations**](InboxApi.md#list_inbox_conversations) | **GET** /{workspaceUuid}/inbox/conversations | List inbox conversations |
| [**list_inbox_reply_drafts**](InboxApi.md#list_inbox_reply_drafts) | **GET** /{workspaceUuid}/inbox/drafts | List reply drafts |
| [**reject_inbox_reply_draft**](InboxApi.md#reject_inbox_reply_draft) | **POST** /{workspaceUuid}/inbox/drafts/{draftId}/reject | Reject a reply draft |
| [**update_inbox_conversation**](InboxApi.md#update_inbox_conversation) | **PATCH** /{workspaceUuid}/inbox/conversations/{conversationId} | Update an inbox conversation |
| [**update_inbox_reply_draft**](InboxApi.md#update_inbox_reply_draft) | **PUT** /{workspaceUuid}/inbox/drafts/{draftId} | Edit a reply draft |


## approve_inbox_reply_draft

> <CreateInboxReplyDraft201Response> approve_inbox_reply_draft(workspace_uuid, draft_id, opts)

Approve and send a reply draft

Sends the draft to the network (optionally with an edited `body`). Ends as `sent`, or `failed` with `error`. Needs the `publish` ability; the API key that wrote the draft cannot approve it (`403`, `code: self_approval`). A draft is sent at most once: approving again returns `409`. Requires the inbox API to be enabled for the workspace (otherwise `404`). Admins and members only. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::InboxApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
draft_id = 'draft_id_example' # String | The draft `id`.
opts = {
  inbox_reply_draft_approve: PostBoost::InboxReplyDraftApprove.new # InboxReplyDraftApprove | 
}

begin
  # Approve and send a reply draft
  result = api_instance.approve_inbox_reply_draft(workspace_uuid, draft_id, opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling InboxApi->approve_inbox_reply_draft: #{e}"
end
```

#### Using the approve_inbox_reply_draft_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateInboxReplyDraft201Response>, Integer, Hash)> approve_inbox_reply_draft_with_http_info(workspace_uuid, draft_id, opts)

```ruby
begin
  # Approve and send a reply draft
  data, status_code, headers = api_instance.approve_inbox_reply_draft_with_http_info(workspace_uuid, draft_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateInboxReplyDraft201Response>
rescue PostBoost::ApiError => e
  puts "Error when calling InboxApi->approve_inbox_reply_draft_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **draft_id** | **String** | The draft &#x60;id&#x60;. |  |
| **inbox_reply_draft_approve** | [**InboxReplyDraftApprove**](InboxReplyDraftApprove.md) |  | [optional] |

### Return type

[**CreateInboxReplyDraft201Response**](CreateInboxReplyDraft201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## create_inbox_reply_draft

> <CreateInboxReplyDraft201Response> create_inbox_reply_draft(workspace_uuid, conversation_id, inbox_reply_draft_input)

Draft a reply

Proposes a reply. Nothing is posted: a person approves the draft in the app (Reply drafts page) or another API key with the `publish` ability approves it. `in_reply_to` defaults to the latest incoming message. The body limit depends on the network (Bluesky 300, Mastodon 500, LinkedIn 1250, Google 4000). Needs the `write` ability. Requires the inbox API to be enabled for the workspace (otherwise `404`). Admins and members only. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::InboxApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
conversation_id = 'conversation_id_example' # String | The conversation `id`.
inbox_reply_draft_input = PostBoost::InboxReplyDraftInput.new({body: 'body_example'}) # InboxReplyDraftInput | 

begin
  # Draft a reply
  result = api_instance.create_inbox_reply_draft(workspace_uuid, conversation_id, inbox_reply_draft_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling InboxApi->create_inbox_reply_draft: #{e}"
end
```

#### Using the create_inbox_reply_draft_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateInboxReplyDraft201Response>, Integer, Hash)> create_inbox_reply_draft_with_http_info(workspace_uuid, conversation_id, inbox_reply_draft_input)

```ruby
begin
  # Draft a reply
  data, status_code, headers = api_instance.create_inbox_reply_draft_with_http_info(workspace_uuid, conversation_id, inbox_reply_draft_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateInboxReplyDraft201Response>
rescue PostBoost::ApiError => e
  puts "Error when calling InboxApi->create_inbox_reply_draft_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **conversation_id** | **String** | The conversation &#x60;id&#x60;. |  |
| **inbox_reply_draft_input** | [**InboxReplyDraftInput**](InboxReplyDraftInput.md) |  |  |

### Return type

[**CreateInboxReplyDraft201Response**](CreateInboxReplyDraft201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_inbox_reply_draft

> delete_inbox_reply_draft(workspace_uuid, draft_id)

Withdraw a reply draft

Deletes a pending draft. `409` once it was reviewed. Requires the inbox API to be enabled for the workspace (otherwise `404`). Admins and members only. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::InboxApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
draft_id = 'draft_id_example' # String | The draft `id`.

begin
  # Withdraw a reply draft
  api_instance.delete_inbox_reply_draft(workspace_uuid, draft_id)
rescue PostBoost::ApiError => e
  puts "Error when calling InboxApi->delete_inbox_reply_draft: #{e}"
end
```

#### Using the delete_inbox_reply_draft_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_inbox_reply_draft_with_http_info(workspace_uuid, draft_id)

```ruby
begin
  # Withdraw a reply draft
  data, status_code, headers = api_instance.delete_inbox_reply_draft_with_http_info(workspace_uuid, draft_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue PostBoost::ApiError => e
  puts "Error when calling InboxApi->delete_inbox_reply_draft_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **draft_id** | **String** | The draft &#x60;id&#x60;. |  |

### Return type

nil (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_inbox_conversation

> <GetInboxConversation200Response> get_inbox_conversation(workspace_uuid, conversation_id)

Get an inbox conversation

The conversation with its 50 most recent messages, oldest first. Requires the inbox API to be enabled for the workspace (otherwise `404`). Admins and members only. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::InboxApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
conversation_id = 'conversation_id_example' # String | The conversation `id`.

begin
  # Get an inbox conversation
  result = api_instance.get_inbox_conversation(workspace_uuid, conversation_id)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling InboxApi->get_inbox_conversation: #{e}"
end
```

#### Using the get_inbox_conversation_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetInboxConversation200Response>, Integer, Hash)> get_inbox_conversation_with_http_info(workspace_uuid, conversation_id)

```ruby
begin
  # Get an inbox conversation
  data, status_code, headers = api_instance.get_inbox_conversation_with_http_info(workspace_uuid, conversation_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetInboxConversation200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling InboxApi->get_inbox_conversation_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **conversation_id** | **String** | The conversation &#x60;id&#x60;. |  |

### Return type

[**GetInboxConversation200Response**](GetInboxConversation200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_inbox_reply_draft

> <CreateInboxReplyDraft201Response> get_inbox_reply_draft(workspace_uuid, draft_id)

Get a reply draft

One draft. Poll it to see whether it was approved and sent. Requires the inbox API to be enabled for the workspace (otherwise `404`). Admins and members only. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::InboxApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
draft_id = 'draft_id_example' # String | The draft `id`.

begin
  # Get a reply draft
  result = api_instance.get_inbox_reply_draft(workspace_uuid, draft_id)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling InboxApi->get_inbox_reply_draft: #{e}"
end
```

#### Using the get_inbox_reply_draft_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateInboxReplyDraft201Response>, Integer, Hash)> get_inbox_reply_draft_with_http_info(workspace_uuid, draft_id)

```ruby
begin
  # Get a reply draft
  data, status_code, headers = api_instance.get_inbox_reply_draft_with_http_info(workspace_uuid, draft_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateInboxReplyDraft201Response>
rescue PostBoost::ApiError => e
  puts "Error when calling InboxApi->get_inbox_reply_draft_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **draft_id** | **String** | The draft &#x60;id&#x60;. |  |

### Return type

[**CreateInboxReplyDraft201Response**](CreateInboxReplyDraft201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_inbox_conversations

> <ListInboxConversations200Response> list_inbox_conversations(workspace_uuid, opts)

List inbox conversations

Comments, mentions and reviews on your accounts, most recent activity first, 25 per page. Available for Bluesky, Mastodon, LinkedIn Pages and Google Business Profile. Requires the inbox API to be enabled for the workspace (otherwise `404`). Admins and members only. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::InboxApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
opts = {
  status: 'open', # String | Conversation status.
  account_id: 56, # Integer | Account `id`.
  provider: 'provider_example', # String | Network, for example `bluesky`.
  unread: true, # Boolean | Only unread (`true`) or read (`false`) conversations.
  sentiment: 'negative', # String | AI sentiment.
  ai_label: 'question', # String | AI label.
  since: Time.parse('2013-10-20T19:20:30+01:00'), # Time | Only conversations with activity at or after this time.
  page: 56 # Integer | Page number.
}

begin
  # List inbox conversations
  result = api_instance.list_inbox_conversations(workspace_uuid, opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling InboxApi->list_inbox_conversations: #{e}"
end
```

#### Using the list_inbox_conversations_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListInboxConversations200Response>, Integer, Hash)> list_inbox_conversations_with_http_info(workspace_uuid, opts)

```ruby
begin
  # List inbox conversations
  data, status_code, headers = api_instance.list_inbox_conversations_with_http_info(workspace_uuid, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListInboxConversations200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling InboxApi->list_inbox_conversations_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **status** | **String** | Conversation status. | [optional] |
| **account_id** | **Integer** | Account &#x60;id&#x60;. | [optional] |
| **provider** | **String** | Network, for example &#x60;bluesky&#x60;. | [optional] |
| **unread** | **Boolean** | Only unread (&#x60;true&#x60;) or read (&#x60;false&#x60;) conversations. | [optional] |
| **sentiment** | **String** | AI sentiment. | [optional] |
| **ai_label** | **String** | AI label. | [optional] |
| **since** | **Time** | Only conversations with activity at or after this time. | [optional] |
| **page** | **Integer** | Page number. | [optional][default to 1] |

### Return type

[**ListInboxConversations200Response**](ListInboxConversations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_inbox_reply_drafts

> <ListInboxReplyDrafts200Response> list_inbox_reply_drafts(workspace_uuid, opts)

List reply drafts

Reply drafts, newest first, 25 per page. Requires the inbox API to be enabled for the workspace (otherwise `404`). Admins and members only. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::InboxApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
opts = {
  status: 'pending', # String | Draft status.
  conversation_id: 'conversation_id_example', # String | Only drafts for this conversation `id`.
  page: 56 # Integer | Page number.
}

begin
  # List reply drafts
  result = api_instance.list_inbox_reply_drafts(workspace_uuid, opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling InboxApi->list_inbox_reply_drafts: #{e}"
end
```

#### Using the list_inbox_reply_drafts_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListInboxReplyDrafts200Response>, Integer, Hash)> list_inbox_reply_drafts_with_http_info(workspace_uuid, opts)

```ruby
begin
  # List reply drafts
  data, status_code, headers = api_instance.list_inbox_reply_drafts_with_http_info(workspace_uuid, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListInboxReplyDrafts200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling InboxApi->list_inbox_reply_drafts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **status** | **String** | Draft status. | [optional] |
| **conversation_id** | **String** | Only drafts for this conversation &#x60;id&#x60;. | [optional] |
| **page** | **Integer** | Page number. | [optional][default to 1] |

### Return type

[**ListInboxReplyDrafts200Response**](ListInboxReplyDrafts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## reject_inbox_reply_draft

> <CreateInboxReplyDraft201Response> reject_inbox_reply_draft(workspace_uuid, draft_id)

Reject a reply draft

Rejects a pending draft; nothing is sent. Needs the `publish` ability. Requires the inbox API to be enabled for the workspace (otherwise `404`). Admins and members only. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::InboxApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
draft_id = 'draft_id_example' # String | The draft `id`.

begin
  # Reject a reply draft
  result = api_instance.reject_inbox_reply_draft(workspace_uuid, draft_id)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling InboxApi->reject_inbox_reply_draft: #{e}"
end
```

#### Using the reject_inbox_reply_draft_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateInboxReplyDraft201Response>, Integer, Hash)> reject_inbox_reply_draft_with_http_info(workspace_uuid, draft_id)

```ruby
begin
  # Reject a reply draft
  data, status_code, headers = api_instance.reject_inbox_reply_draft_with_http_info(workspace_uuid, draft_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateInboxReplyDraft201Response>
rescue PostBoost::ApiError => e
  puts "Error when calling InboxApi->reject_inbox_reply_draft_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **draft_id** | **String** | The draft &#x60;id&#x60;. |  |

### Return type

[**CreateInboxReplyDraft201Response**](CreateInboxReplyDraft201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_inbox_conversation

> <GetInboxConversation200Response> update_inbox_conversation(workspace_uuid, conversation_id, inbox_conversation_update)

Update an inbox conversation

Marks the conversation open or resolved, read or unread. Requires the inbox API to be enabled for the workspace (otherwise `404`). Admins and members only. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::InboxApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
conversation_id = 'conversation_id_example' # String | The conversation `id`.
inbox_conversation_update = PostBoost::InboxConversationUpdate.new # InboxConversationUpdate | 

begin
  # Update an inbox conversation
  result = api_instance.update_inbox_conversation(workspace_uuid, conversation_id, inbox_conversation_update)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling InboxApi->update_inbox_conversation: #{e}"
end
```

#### Using the update_inbox_conversation_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetInboxConversation200Response>, Integer, Hash)> update_inbox_conversation_with_http_info(workspace_uuid, conversation_id, inbox_conversation_update)

```ruby
begin
  # Update an inbox conversation
  data, status_code, headers = api_instance.update_inbox_conversation_with_http_info(workspace_uuid, conversation_id, inbox_conversation_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetInboxConversation200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling InboxApi->update_inbox_conversation_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **conversation_id** | **String** | The conversation &#x60;id&#x60;. |  |
| **inbox_conversation_update** | [**InboxConversationUpdate**](InboxConversationUpdate.md) |  |  |

### Return type

[**GetInboxConversation200Response**](GetInboxConversation200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_inbox_reply_draft

> <CreateInboxReplyDraft201Response> update_inbox_reply_draft(workspace_uuid, draft_id, inbox_reply_draft_edit)

Edit a reply draft

Changes the text of a pending draft. `409` once it was reviewed. Requires the inbox API to be enabled for the workspace (otherwise `404`). Admins and members only. 

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::InboxApi.new
workspace_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the workspace.
draft_id = 'draft_id_example' # String | The draft `id`.
inbox_reply_draft_edit = PostBoost::InboxReplyDraftEdit.new({body: 'body_example'}) # InboxReplyDraftEdit | 

begin
  # Edit a reply draft
  result = api_instance.update_inbox_reply_draft(workspace_uuid, draft_id, inbox_reply_draft_edit)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling InboxApi->update_inbox_reply_draft: #{e}"
end
```

#### Using the update_inbox_reply_draft_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateInboxReplyDraft201Response>, Integer, Hash)> update_inbox_reply_draft_with_http_info(workspace_uuid, draft_id, inbox_reply_draft_edit)

```ruby
begin
  # Edit a reply draft
  data, status_code, headers = api_instance.update_inbox_reply_draft_with_http_info(workspace_uuid, draft_id, inbox_reply_draft_edit)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateInboxReplyDraft201Response>
rescue PostBoost::ApiError => e
  puts "Error when calling InboxApi->update_inbox_reply_draft_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** | UUID of the workspace. |  |
| **draft_id** | **String** | The draft &#x60;id&#x60;. |  |
| **inbox_reply_draft_edit** | [**InboxReplyDraftEdit**](InboxReplyDraftEdit.md) |  |  |

### Return type

[**CreateInboxReplyDraft201Response**](CreateInboxReplyDraft201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

