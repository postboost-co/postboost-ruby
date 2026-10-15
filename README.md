# PostBoost Ruby SDK

Official Ruby client for the [PostBoost API](https://postboost.co/docs/api).

## Install

```bash
gem install postboost
```

| | |
|---|---|
| **RubyGems** | [rubygems.org/gems/postboost](https://rubygems.org/gems/postboost) |
| **GitHub** | [postboost-co/postboost-ruby](https://github.com/postboost-co/postboost-ruby) |
| **Docs** | [postboost.co/docs/api](https://postboost.co/docs/api) |
| **Version** | v1.26.2 |

## Quick start

```ruby
require 'postboost'

PostBoost.configure { |c| c.access_token = ENV['POSTBOOST_API_TOKEN'] }

api = PostBoost::PostsApi.new
posts = api.list_posts('YOUR_WORKSPACE_UUID')
posts.each { |p| puts p.uuid }
```

---

## Documentation for API Endpoints

All URIs are relative to *https://postboost.co/app/api*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*PostBoost::AIApi* | [**blog_to_social**](docs/AIApi.md#blog_to_social) | **POST** /{workspaceUuid}/ai/blog-to-social | Generate social media captions from a blog post
*PostBoost::AIApi* | [**delete_brand_voice**](docs/AIApi.md#delete_brand_voice) | **DELETE** /{workspaceUuid}/brand-voice | Delete the brand voice
*PostBoost::AIApi* | [**get_ai_usage**](docs/AIApi.md#get_ai_usage) | **GET** /{workspaceUuid}/usage/ai | AI credit usage
*PostBoost::AIApi* | [**get_brand_voice**](docs/AIApi.md#get_brand_voice) | **GET** /{workspaceUuid}/brand-voice | Get the brand voice
*PostBoost::AIApi* | [**get_repurpose_run**](docs/AIApi.md#get_repurpose_run) | **GET** /{workspaceUuid}/ai/repurpose/runs/{runId} | Get a repurpose run
*PostBoost::AIApi* | [**image_alt_text**](docs/AIApi.md#image_alt_text) | **POST** /{workspaceUuid}/ai/image-alt-text | Generate alt text for a media image using AI
*PostBoost::AIApi* | [**image_edit**](docs/AIApi.md#image_edit) | **POST** /{workspaceUuid}/ai/image-edit | Edit an existing media image using AI
*PostBoost::AIApi* | [**image_generate**](docs/AIApi.md#image_generate) | **POST** /{workspaceUuid}/ai/image-generate | Generate social media images from a caption
*PostBoost::AIApi* | [**image_prompt**](docs/AIApi.md#image_prompt) | **POST** /{workspaceUuid}/ai/image-prompt | Build an optimized image prompt from a social media caption
*PostBoost::AIApi* | [**image_variations**](docs/AIApi.md#image_variations) | **POST** /{workspaceUuid}/ai/image-variations | Generate variations of an existing media image
*PostBoost::AIApi* | [**learn_brand_voice**](docs/AIApi.md#learn_brand_voice) | **POST** /{workspaceUuid}/brand-voice/learn | Learn a brand voice from past posts
*PostBoost::AIApi* | [**repurpose_content**](docs/AIApi.md#repurpose_content) | **POST** /{workspaceUuid}/ai/repurpose | Repurpose long-form content into a draft post set with a carousel
*PostBoost::AIApi* | [**update_brand_voice**](docs/AIApi.md#update_brand_voice) | **PUT** /{workspaceUuid}/brand-voice | Create or update the brand voice
*PostBoost::AccountGroupsApi* | [**create_account_group**](docs/AccountGroupsApi.md#create_account_group) | **POST** /{workspaceUuid}/account-groups | Create an account group
*PostBoost::AccountGroupsApi* | [**delete_account_group**](docs/AccountGroupsApi.md#delete_account_group) | **DELETE** /{workspaceUuid}/account-groups/{accountGroupUuid} | Delete an account group
*PostBoost::AccountGroupsApi* | [**get_account_group**](docs/AccountGroupsApi.md#get_account_group) | **GET** /{workspaceUuid}/account-groups/{accountGroupUuid} | Get an account group
*PostBoost::AccountGroupsApi* | [**list_account_groups**](docs/AccountGroupsApi.md#list_account_groups) | **GET** /{workspaceUuid}/account-groups | List account groups
*PostBoost::AccountGroupsApi* | [**update_account_group**](docs/AccountGroupsApi.md#update_account_group) | **PUT** /{workspaceUuid}/account-groups/{accountGroupUuid} | Update an account group
*PostBoost::AccountsApi* | [**connect_channel**](docs/AccountsApi.md#connect_channel) | **POST** /{workspaceUuid}/accounts/connect/{provider} | Connect a Telegram, Discord or Slack channel
*PostBoost::AccountsApi* | [**create_connect_link**](docs/AccountsApi.md#create_connect_link) | **POST** /{workspaceUuid}/accounts/connect-links | Create a connect link
*PostBoost::AccountsApi* | [**create_reconnect_link**](docs/AccountsApi.md#create_reconnect_link) | **POST** /{workspaceUuid}/accounts/{accountUuid}/reconnect-links | Create a reconnect link
*PostBoost::AccountsApi* | [**get_account**](docs/AccountsApi.md#get_account) | **GET** /{workspaceUuid}/accounts/{accountUuid} | Get account
*PostBoost::AccountsApi* | [**get_account_health**](docs/AccountsApi.md#get_account_health) | **GET** /{workspaceUuid}/account-health | Account health
*PostBoost::AccountsApi* | [**list_accounts**](docs/AccountsApi.md#list_accounts) | **GET** /{workspaceUuid}/accounts | List accounts
*PostBoost::ActivityApi* | [**list_api_activity**](docs/ActivityApi.md#list_api_activity) | **GET** /{workspaceUuid}/activity | List API activity
*PostBoost::AgentsApi* | [**approve_agent_proposal**](docs/AgentsApi.md#approve_agent_proposal) | **POST** /{workspaceUuid}/agent-proposals/{proposalUuid}/approve | Approve and apply an agent proposal
*PostBoost::AgentsApi* | [**create_agent**](docs/AgentsApi.md#create_agent) | **POST** /{workspaceUuid}/agents | Switch on a background agent
*PostBoost::AgentsApi* | [**delete_agent**](docs/AgentsApi.md#delete_agent) | **DELETE** /{workspaceUuid}/agents/{agentUuid} | Delete a background agent
*PostBoost::AgentsApi* | [**get_agent_run**](docs/AgentsApi.md#get_agent_run) | **GET** /{workspaceUuid}/agent-runs/{runUuid} | Get an agent run with its proposals
*PostBoost::AgentsApi* | [**list_agent_proposals**](docs/AgentsApi.md#list_agent_proposals) | **GET** /{workspaceUuid}/agent-proposals | List agent proposals (approval queue)
*PostBoost::AgentsApi* | [**list_agent_runs**](docs/AgentsApi.md#list_agent_runs) | **GET** /{workspaceUuid}/agents/{agentUuid}/runs | Run history of an agent
*PostBoost::AgentsApi* | [**list_agents**](docs/AgentsApi.md#list_agents) | **GET** /{workspaceUuid}/agents | List background agents
*PostBoost::AgentsApi* | [**reject_agent_proposal**](docs/AgentsApi.md#reject_agent_proposal) | **POST** /{workspaceUuid}/agent-proposals/{proposalUuid}/reject | Reject an agent proposal
*PostBoost::AgentsApi* | [**run_agent**](docs/AgentsApi.md#run_agent) | **POST** /{workspaceUuid}/agents/{agentUuid}/run | Run a background agent now
*PostBoost::AgentsApi* | [**update_agent**](docs/AgentsApi.md#update_agent) | **PUT** /{workspaceUuid}/agents/{agentUuid} | Update a background agent
*PostBoost::AnalyticsApi* | [**create_report_export**](docs/AnalyticsApi.md#create_report_export) | **POST** /{workspaceUuid}/reports/exports | Create a report export
*PostBoost::AnalyticsApi* | [**download_report_export**](docs/AnalyticsApi.md#download_report_export) | **GET** /{workspaceUuid}/reports/exports/{exportUuid}/download | Download a report file
*PostBoost::AnalyticsApi* | [**get_account_analytics**](docs/AnalyticsApi.md#get_account_analytics) | **GET** /{workspaceUuid}/analytics/accounts/{accountUuid} | Get account analytics
*PostBoost::AnalyticsApi* | [**get_analytics_summary**](docs/AnalyticsApi.md#get_analytics_summary) | **GET** /{workspaceUuid}/analytics | Get analytics summary
*PostBoost::AnalyticsApi* | [**get_best_posting_times**](docs/AnalyticsApi.md#get_best_posting_times) | **GET** /{workspaceUuid}/analytics/best-times | Get best posting times
*PostBoost::AnalyticsApi* | [**get_post_analytics_0**](docs/AnalyticsApi.md#get_post_analytics_0) | **GET** /{workspaceUuid}/posts/{postUuid}/analytics | Get post analytics
*PostBoost::AnalyticsApi* | [**get_posting_times**](docs/AnalyticsApi.md#get_posting_times) | **GET** /{workspaceUuid}/analytics/posting-times | Get posting times heatmap
*PostBoost::AnalyticsApi* | [**get_report_branding**](docs/AnalyticsApi.md#get_report_branding) | **GET** /{workspaceUuid}/report-branding | Get the report branding
*PostBoost::AnalyticsApi* | [**get_report_export**](docs/AnalyticsApi.md#get_report_export) | **GET** /{workspaceUuid}/reports/exports/{exportUuid} | Get a report export
*PostBoost::AnalyticsApi* | [**list_report_exports**](docs/AnalyticsApi.md#list_report_exports) | **GET** /{workspaceUuid}/reports/exports | List report exports
*PostBoost::AnalyticsApi* | [**update_report_branding**](docs/AnalyticsApi.md#update_report_branding) | **PUT** /{workspaceUuid}/report-branding | Update the report branding
*PostBoost::AnalyticsApi* | [**upload_report_branding_logo**](docs/AnalyticsApi.md#upload_report_branding_logo) | **POST** /{workspaceUuid}/report-branding/logo | Upload the report logo
*PostBoost::CompetitorsApi* | [**add_competitor**](docs/CompetitorsApi.md#add_competitor) | **POST** /{workspaceUuid}/competitors | Track a competitor
*PostBoost::CompetitorsApi* | [**delete_competitor**](docs/CompetitorsApi.md#delete_competitor) | **DELETE** /{workspaceUuid}/competitors/{competitorId} | Stop tracking a competitor
*PostBoost::CompetitorsApi* | [**get_competitor**](docs/CompetitorsApi.md#get_competitor) | **GET** /{workspaceUuid}/competitors/{competitorId} | Get a competitor
*PostBoost::CompetitorsApi* | [**list_competitors**](docs/CompetitorsApi.md#list_competitors) | **GET** /{workspaceUuid}/competitors | List competitors
*PostBoost::FreeToolsApi* | [**build_utm_url**](docs/FreeToolsApi.md#build_utm_url) | **POST** /tools/utm-builder | Build a UTM-tagged campaign URL
*PostBoost::FreeToolsApi* | [**calculate_engagement_rate**](docs/FreeToolsApi.md#calculate_engagement_rate) | **POST** /tools/engagement-rate-calculator | Calculate an engagement rate
*PostBoost::FreeToolsApi* | [**clean_text**](docs/FreeToolsApi.md#clean_text) | **POST** /tools/ai-text-cleaner | Clean AI-written text: dashes, quotes, invisible characters, markdown
*PostBoost::FreeToolsApi* | [**count_characters**](docs/FreeToolsApi.md#count_characters) | **POST** /tools/social-media-character-counter | Count characters as each network counts them
*PostBoost::FreeToolsApi* | [**format_linked_in_post**](docs/FreeToolsApi.md#format_linked_in_post) | **POST** /tools/linkedin-post-formatter | Format a LinkedIn post with bold, italic and lists
*PostBoost::FreeToolsApi* | [**generate_fancy_text**](docs/FreeToolsApi.md#generate_fancy_text) | **POST** /tools/fancy-text-generator | Convert text to fancy Unicode styles
*PostBoost::FreeToolsApi* | [**list_free_tools**](docs/FreeToolsApi.md#list_free_tools) | **GET** /tools | List the free tools
*PostBoost::FreeToolsApi* | [**split_thread**](docs/FreeToolsApi.md#split_thread) | **POST** /tools/x-thread-maker | Split long text into a thread
*PostBoost::HashtagGroupsApi* | [**create_hashtag_group**](docs/HashtagGroupsApi.md#create_hashtag_group) | **POST** /{workspaceUuid}/hashtag-groups | Create a hashtag group
*PostBoost::HashtagGroupsApi* | [**delete_hashtag_group**](docs/HashtagGroupsApi.md#delete_hashtag_group) | **DELETE** /{workspaceUuid}/hashtag-groups/{hashtagGroupId} | Delete a hashtag group
*PostBoost::HashtagGroupsApi* | [**get_hashtag_group**](docs/HashtagGroupsApi.md#get_hashtag_group) | **GET** /{workspaceUuid}/hashtag-groups/{hashtagGroupId} | Get a hashtag group
*PostBoost::HashtagGroupsApi* | [**list_hashtag_groups**](docs/HashtagGroupsApi.md#list_hashtag_groups) | **GET** /{workspaceUuid}/hashtag-groups | List hashtag groups
*PostBoost::HashtagGroupsApi* | [**update_hashtag_group**](docs/HashtagGroupsApi.md#update_hashtag_group) | **PUT** /{workspaceUuid}/hashtag-groups/{hashtagGroupId} | Update a hashtag group
*PostBoost::InboxApi* | [**approve_inbox_reply_draft**](docs/InboxApi.md#approve_inbox_reply_draft) | **POST** /{workspaceUuid}/inbox/drafts/{draftId}/approve | Approve and send a reply draft
*PostBoost::InboxApi* | [**create_inbox_reply_draft**](docs/InboxApi.md#create_inbox_reply_draft) | **POST** /{workspaceUuid}/inbox/conversations/{conversationId}/drafts | Draft a reply
*PostBoost::InboxApi* | [**delete_inbox_reply_draft**](docs/InboxApi.md#delete_inbox_reply_draft) | **DELETE** /{workspaceUuid}/inbox/drafts/{draftId} | Withdraw a reply draft
*PostBoost::InboxApi* | [**get_inbox_conversation**](docs/InboxApi.md#get_inbox_conversation) | **GET** /{workspaceUuid}/inbox/conversations/{conversationId} | Get an inbox conversation
*PostBoost::InboxApi* | [**get_inbox_reply_draft**](docs/InboxApi.md#get_inbox_reply_draft) | **GET** /{workspaceUuid}/inbox/drafts/{draftId} | Get a reply draft
*PostBoost::InboxApi* | [**list_inbox_conversations**](docs/InboxApi.md#list_inbox_conversations) | **GET** /{workspaceUuid}/inbox/conversations | List inbox conversations
*PostBoost::InboxApi* | [**list_inbox_reply_drafts**](docs/InboxApi.md#list_inbox_reply_drafts) | **GET** /{workspaceUuid}/inbox/drafts | List reply drafts
*PostBoost::InboxApi* | [**reject_inbox_reply_draft**](docs/InboxApi.md#reject_inbox_reply_draft) | **POST** /{workspaceUuid}/inbox/drafts/{draftId}/reject | Reject a reply draft
*PostBoost::InboxApi* | [**update_inbox_conversation**](docs/InboxApi.md#update_inbox_conversation) | **PATCH** /{workspaceUuid}/inbox/conversations/{conversationId} | Update an inbox conversation
*PostBoost::InboxApi* | [**update_inbox_reply_draft**](docs/InboxApi.md#update_inbox_reply_draft) | **PUT** /{workspaceUuid}/inbox/drafts/{draftId} | Edit a reply draft
*PostBoost::MediaApi* | [**abort_chunked_upload**](docs/MediaApi.md#abort_chunked_upload) | **DELETE** /{workspaceUuid}/media/chunked/{uploadUuid} | Abort chunked upload
*PostBoost::MediaApi* | [**complete_chunked_upload**](docs/MediaApi.md#complete_chunked_upload) | **POST** /{workspaceUuid}/media/chunked/{uploadUuid}/complete | Complete chunked upload
*PostBoost::MediaApi* | [**create_media_folder**](docs/MediaApi.md#create_media_folder) | **POST** /{workspaceUuid}/media/folders | Create media folder
*PostBoost::MediaApi* | [**delete_media_bulk**](docs/MediaApi.md#delete_media_bulk) | **DELETE** /{workspaceUuid}/media | Delete media (bulk)
*PostBoost::MediaApi* | [**delete_media_folder**](docs/MediaApi.md#delete_media_folder) | **DELETE** /{workspaceUuid}/media/folders/{folderUuid} | Delete media folder
*PostBoost::MediaApi* | [**get_media**](docs/MediaApi.md#get_media) | **GET** /{workspaceUuid}/media/{mediaUuid} | Get media
*PostBoost::MediaApi* | [**get_remote_upload_status**](docs/MediaApi.md#get_remote_upload_status) | **GET** /{workspaceUuid}/media/remote/{downloadId}/status | Get remote upload status
*PostBoost::MediaApi* | [**initiate_chunked_upload**](docs/MediaApi.md#initiate_chunked_upload) | **POST** /{workspaceUuid}/media/chunked/initiate | Initiate chunked upload
*PostBoost::MediaApi* | [**initiate_remote_upload**](docs/MediaApi.md#initiate_remote_upload) | **POST** /{workspaceUuid}/media/remote/initiate | Initiate remote upload
*PostBoost::MediaApi* | [**list_media**](docs/MediaApi.md#list_media) | **GET** /{workspaceUuid}/media | List media
*PostBoost::MediaApi* | [**list_media_folders**](docs/MediaApi.md#list_media_folders) | **GET** /{workspaceUuid}/media/folders | List media folders
*PostBoost::MediaApi* | [**update_media**](docs/MediaApi.md#update_media) | **PUT** /{workspaceUuid}/media/{mediaUuid} | Update media
*PostBoost::MediaApi* | [**update_media_folder**](docs/MediaApi.md#update_media_folder) | **PUT** /{workspaceUuid}/media/folders/{folderUuid} | Update media folder
*PostBoost::MediaApi* | [**upload_chunk**](docs/MediaApi.md#upload_chunk) | **POST** /{workspaceUuid}/media/chunked/{uploadUuid}/upload | Upload a chunk
*PostBoost::MediaApi* | [**upload_media**](docs/MediaApi.md#upload_media) | **POST** /{workspaceUuid}/media | Upload media (binary)
*PostBoost::MediaApi* | [**upload_media_base64**](docs/MediaApi.md#upload_media_base64) | **POST** /{workspaceUuid}/media/base64 | Upload media (base64 JSON)
*PostBoost::MentionsApi* | [**create_mention**](docs/MentionsApi.md#create_mention) | **POST** /{workspaceUuid}/mentions | Create mention
*PostBoost::MentionsApi* | [**delete_mention**](docs/MentionsApi.md#delete_mention) | **DELETE** /{workspaceUuid}/mentions/{mentionId} | Delete mention
*PostBoost::MentionsApi* | [**get_mention**](docs/MentionsApi.md#get_mention) | **GET** /{workspaceUuid}/mentions/{mentionId} | Get mention
*PostBoost::MentionsApi* | [**list_mentions**](docs/MentionsApi.md#list_mentions) | **GET** /{workspaceUuid}/mentions | List mentions
*PostBoost::MentionsApi* | [**update_mention**](docs/MentionsApi.md#update_mention) | **PUT** /{workspaceUuid}/mentions/{mentionId} | Update mention
*PostBoost::PostingScheduleApi* | [**get_posting_schedule**](docs/PostingScheduleApi.md#get_posting_schedule) | **GET** /{workspaceUuid}/posting-schedule | Get the posting schedule
*PostBoost::PostingScheduleApi* | [**get_recommended_posting_times**](docs/PostingScheduleApi.md#get_recommended_posting_times) | **GET** /{workspaceUuid}/posting-schedule/recommended | Get recommended posting times
*PostBoost::PostingScheduleApi* | [**list_queue_slots**](docs/PostingScheduleApi.md#list_queue_slots) | **GET** /{workspaceUuid}/queue/slots | List upcoming queue slots
*PostBoost::PostingScheduleApi* | [**reset_account_posting_schedule**](docs/PostingScheduleApi.md#reset_account_posting_schedule) | **DELETE** /{workspaceUuid}/posting-schedule/{accountId} | Reset an account schedule
*PostBoost::PostingScheduleApi* | [**update_posting_schedule**](docs/PostingScheduleApi.md#update_posting_schedule) | **PUT** /{workspaceUuid}/posting-schedule | Set the posting schedule
*PostBoost::PostsApi* | [**add_post_to_queue**](docs/PostsApi.md#add_post_to_queue) | **POST** /{workspaceUuid}/posts/add-to-queue/{postUuid} | Add post to queue
*PostBoost::PostsApi* | [**approve_post**](docs/PostsApi.md#approve_post) | **POST** /{workspaceUuid}/posts/approve/{postUuid} | Approve post
*PostBoost::PostsApi* | [**create_post**](docs/PostsApi.md#create_post) | **POST** /{workspaceUuid}/posts | Create post
*PostBoost::PostsApi* | [**create_recycling_rule**](docs/PostsApi.md#create_recycling_rule) | **POST** /{workspaceUuid}/recycling-rules | Create a recycling rule
*PostBoost::PostsApi* | [**create_rss_feed**](docs/PostsApi.md#create_rss_feed) | **POST** /{workspaceUuid}/rss-feeds | Add an RSS feed
*PostBoost::PostsApi* | [**delete_post**](docs/PostsApi.md#delete_post) | **DELETE** /{workspaceUuid}/posts/{postUuid} | Delete post
*PostBoost::PostsApi* | [**delete_posts_bulk**](docs/PostsApi.md#delete_posts_bulk) | **DELETE** /{workspaceUuid}/posts | Delete posts (bulk)
*PostBoost::PostsApi* | [**delete_recycling_rule**](docs/PostsApi.md#delete_recycling_rule) | **DELETE** /{workspaceUuid}/recycling-rules/{ruleUuid} | Delete a recycling rule
*PostBoost::PostsApi* | [**delete_rss_feed**](docs/PostsApi.md#delete_rss_feed) | **DELETE** /{workspaceUuid}/rss-feeds/{feedUuid} | Delete an RSS feed
*PostBoost::PostsApi* | [**get_post**](docs/PostsApi.md#get_post) | **GET** /{workspaceUuid}/posts/{postUuid} | Get post
*PostBoost::PostsApi* | [**get_post_analytics**](docs/PostsApi.md#get_post_analytics) | **GET** /{workspaceUuid}/posts/{postUuid}/analytics | Get post analytics
*PostBoost::PostsApi* | [**get_recycling_rule**](docs/PostsApi.md#get_recycling_rule) | **GET** /{workspaceUuid}/recycling-rules/{ruleUuid} | Get a recycling rule
*PostBoost::PostsApi* | [**get_rss_feed**](docs/PostsApi.md#get_rss_feed) | **GET** /{workspaceUuid}/rss-feeds/{feedUuid} | Get an RSS feed
*PostBoost::PostsApi* | [**list_posts**](docs/PostsApi.md#list_posts) | **GET** /{workspaceUuid}/posts | List posts
*PostBoost::PostsApi* | [**list_recycling_rules**](docs/PostsApi.md#list_recycling_rules) | **GET** /{workspaceUuid}/recycling-rules | List recycling rules
*PostBoost::PostsApi* | [**list_recycling_runs**](docs/PostsApi.md#list_recycling_runs) | **GET** /{workspaceUuid}/recycling-rules/{ruleUuid}/runs | List a recycling rule's runs
*PostBoost::PostsApi* | [**list_rss_feeds**](docs/PostsApi.md#list_rss_feeds) | **GET** /{workspaceUuid}/rss-feeds | List RSS feeds
*PostBoost::PostsApi* | [**poll_rss_feed**](docs/PostsApi.md#poll_rss_feed) | **POST** /{workspaceUuid}/rss-feeds/{feedUuid}/poll | Check an RSS feed now
*PostBoost::PostsApi* | [**recycle_post**](docs/PostsApi.md#recycle_post) | **POST** /{workspaceUuid}/posts/{postUuid}/recycle | Recycle a post on an interval
*PostBoost::PostsApi* | [**retry_post_account**](docs/PostsApi.md#retry_post_account) | **POST** /{workspaceUuid}/posts/retry/{postUuid}/{accountUuid} | Retry publishing to one account
*PostBoost::PostsApi* | [**schedule_post**](docs/PostsApi.md#schedule_post) | **POST** /{workspaceUuid}/posts/schedule/{postUuid} | Schedule post
*PostBoost::PostsApi* | [**update_post**](docs/PostsApi.md#update_post) | **PUT** /{workspaceUuid}/posts/{postUuid} | Update post
*PostBoost::PostsApi* | [**update_recycling_rule**](docs/PostsApi.md#update_recycling_rule) | **PUT** /{workspaceUuid}/recycling-rules/{ruleUuid} | Update, pause or resume a recycling rule
*PostBoost::PostsApi* | [**update_rss_feed**](docs/PostsApi.md#update_rss_feed) | **PUT** /{workspaceUuid}/rss-feeds/{feedUuid} | Update, pause or resume an RSS feed
*PostBoost::PostsApi* | [**validate_post**](docs/PostsApi.md#validate_post) | **POST** /{workspaceUuid}/posts/validate | Validate post (dry run)
*PostBoost::ReceiptsApi* | [**create_receipt**](docs/ReceiptsApi.md#create_receipt) | **POST** /panel/receipts | Create receipt
*PostBoost::ReceiptsApi* | [**delete_receipt**](docs/ReceiptsApi.md#delete_receipt) | **DELETE** /panel/receipts/{receiptUuid} | Delete receipt
*PostBoost::ReceiptsApi* | [**delete_receipts_bulk**](docs/ReceiptsApi.md#delete_receipts_bulk) | **DELETE** /panel/receipts | Delete receipts (bulk)
*PostBoost::ReceiptsApi* | [**get_receipt**](docs/ReceiptsApi.md#get_receipt) | **GET** /panel/receipts/{receiptUuid} | Get receipt
*PostBoost::ReceiptsApi* | [**list_receipts**](docs/ReceiptsApi.md#list_receipts) | **GET** /panel/receipts | List receipts
*PostBoost::ReceiptsApi* | [**update_receipt**](docs/ReceiptsApi.md#update_receipt) | **PUT** /panel/receipts/{receiptUuid} | Update receipt
*PostBoost::SubscriptionsApi* | [**add_generic_subscription**](docs/SubscriptionsApi.md#add_generic_subscription) | **POST** /panel/workspaces/{workspaceUuid}/subscription/generic | Add generic subscription
*PostBoost::SubscriptionsApi* | [**cancel_subscription**](docs/SubscriptionsApi.md#cancel_subscription) | **POST** /panel/workspaces/{workspaceUuid}/subscription/cancel | Cancel subscription
*PostBoost::SubscriptionsApi* | [**change_subscription_plan**](docs/SubscriptionsApi.md#change_subscription_plan) | **PUT** /panel/workspaces/{workspaceUuid}/subscription/change-plan | Change subscription plan
*PostBoost::SubscriptionsApi* | [**checkout_subscription**](docs/SubscriptionsApi.md#checkout_subscription) | **POST** /panel/workspaces/{workspaceUuid}/subscription/new | New subscription checkout
*PostBoost::SubscriptionsApi* | [**create_subscription**](docs/SubscriptionsApi.md#create_subscription) | **POST** /panel/workspaces/{workspaceUuid}/subscription | Create subscription
*PostBoost::SubscriptionsApi* | [**delete_subscription**](docs/SubscriptionsApi.md#delete_subscription) | **DELETE** /panel/workspaces/{workspaceUuid}/subscription | Delete subscription
*PostBoost::SubscriptionsApi* | [**get_subscription**](docs/SubscriptionsApi.md#get_subscription) | **GET** /panel/workspaces/{workspaceUuid}/subscription | Get subscription
*PostBoost::SubscriptionsApi* | [**remove_generic_subscription**](docs/SubscriptionsApi.md#remove_generic_subscription) | **DELETE** /panel/workspaces/{workspaceUuid}/subscription/generic | Remove generic subscription
*PostBoost::SubscriptionsApi* | [**resume_subscription**](docs/SubscriptionsApi.md#resume_subscription) | **POST** /panel/workspaces/{workspaceUuid}/subscription/resume | Resume subscription
*PostBoost::SubscriptionsApi* | [**update_subscription**](docs/SubscriptionsApi.md#update_subscription) | **PUT** /panel/workspaces/{workspaceUuid}/subscription | Update subscription
*PostBoost::TagsApi* | [**create_tag**](docs/TagsApi.md#create_tag) | **POST** /{workspaceUuid}/tags | Create tag
*PostBoost::TagsApi* | [**delete_tag**](docs/TagsApi.md#delete_tag) | **DELETE** /{workspaceUuid}/tags/{tagUuid} | Delete tag
*PostBoost::TagsApi* | [**get_tag**](docs/TagsApi.md#get_tag) | **GET** /{workspaceUuid}/tags/{tagUuid} | Get tag
*PostBoost::TagsApi* | [**list_tags**](docs/TagsApi.md#list_tags) | **GET** /{workspaceUuid}/tags | List tags
*PostBoost::TagsApi* | [**update_tag**](docs/TagsApi.md#update_tag) | **PUT** /{workspaceUuid}/tags/{tagUuid} | Update tag
*PostBoost::TemplatesApi* | [**create_template**](docs/TemplatesApi.md#create_template) | **POST** /{workspaceUuid}/templates | Create a template
*PostBoost::TemplatesApi* | [**delete_template**](docs/TemplatesApi.md#delete_template) | **DELETE** /{workspaceUuid}/templates/{templateId} | Delete a template
*PostBoost::TemplatesApi* | [**get_template**](docs/TemplatesApi.md#get_template) | **GET** /{workspaceUuid}/templates/{templateId} | Get a template
*PostBoost::TemplatesApi* | [**list_templates**](docs/TemplatesApi.md#list_templates) | **GET** /{workspaceUuid}/templates | List templates
*PostBoost::TemplatesApi* | [**update_template**](docs/TemplatesApi.md#update_template) | **PUT** /{workspaceUuid}/templates/{templateId} | Update a template
*PostBoost::UsersApi* | [**create_user**](docs/UsersApi.md#create_user) | **POST** /panel/users | Create user
*PostBoost::UsersApi* | [**delete_user**](docs/UsersApi.md#delete_user) | **DELETE** /panel/users/{userId} | Delete user
*PostBoost::UsersApi* | [**delete_users_bulk**](docs/UsersApi.md#delete_users_bulk) | **DELETE** /panel/users | Delete users (bulk)
*PostBoost::UsersApi* | [**get_user**](docs/UsersApi.md#get_user) | **GET** /panel/users/{userId} | Get user
*PostBoost::UsersApi* | [**list_users**](docs/UsersApi.md#list_users) | **GET** /panel/users | List users
*PostBoost::UsersApi* | [**update_user**](docs/UsersApi.md#update_user) | **PUT** /panel/users/{userId} | Update user
*PostBoost::WebhooksApi* | [**create_webhook_subscription**](docs/WebhooksApi.md#create_webhook_subscription) | **POST** /{workspaceUuid}/webhooks/subscriptions | Subscribe a webhook
*PostBoost::WebhooksApi* | [**delete_webhook_subscription**](docs/WebhooksApi.md#delete_webhook_subscription) | **DELETE** /{workspaceUuid}/webhooks/subscriptions/{subscriptionUuid} | Unsubscribe a webhook
*PostBoost::WebhooksApi* | [**list_webhook_subscriptions**](docs/WebhooksApi.md#list_webhook_subscriptions) | **GET** /{workspaceUuid}/webhooks/subscriptions | List webhook subscriptions
*PostBoost::WorkspacesApi* | [**add_user_to_workspace**](docs/WorkspacesApi.md#add_user_to_workspace) | **POST** /panel/workspaces/{workspaceUuid}/users | Add user to workspace
*PostBoost::WorkspacesApi* | [**create_api_key**](docs/WorkspacesApi.md#create_api_key) | **POST** /{workspaceUuid}/api-keys | Create a scoped API key
*PostBoost::WorkspacesApi* | [**create_reseller_client**](docs/WorkspacesApi.md#create_reseller_client) | **POST** /{workspaceUuid}/clients | Create a client workspace
*PostBoost::WorkspacesApi* | [**create_workspace**](docs/WorkspacesApi.md#create_workspace) | **POST** /panel/workspaces | Create workspace
*PostBoost::WorkspacesApi* | [**delete_api_key**](docs/WorkspacesApi.md#delete_api_key) | **DELETE** /{workspaceUuid}/api-keys/{apiKeyId} | Revoke a scoped API key
*PostBoost::WorkspacesApi* | [**delete_workspace**](docs/WorkspacesApi.md#delete_workspace) | **DELETE** /panel/workspaces/{workspaceUuid} | Delete workspace
*PostBoost::WorkspacesApi* | [**delete_workspaces_bulk**](docs/WorkspacesApi.md#delete_workspaces_bulk) | **DELETE** /panel/workspaces | Delete workspaces (bulk)
*PostBoost::WorkspacesApi* | [**get_workspace**](docs/WorkspacesApi.md#get_workspace) | **GET** /panel/workspaces/{workspaceUuid} | Get workspace
*PostBoost::WorkspacesApi* | [**get_workspace_ai_credits**](docs/WorkspacesApi.md#get_workspace_ai_credits) | **GET** /panel/workspaces/{workspaceUuid}/ai-credits | Get workspace AI credits
*PostBoost::WorkspacesApi* | [**get_x_usage**](docs/WorkspacesApi.md#get_x_usage) | **GET** /{workspaceUuid}/usage/x | X (Twitter) usage
*PostBoost::WorkspacesApi* | [**list_api_keys**](docs/WorkspacesApi.md#list_api_keys) | **GET** /{workspaceUuid}/api-keys | List scoped API keys
*PostBoost::WorkspacesApi* | [**list_my_workspaces**](docs/WorkspacesApi.md#list_my_workspaces) | **GET** /workspaces | List my workspaces
*PostBoost::WorkspacesApi* | [**list_reseller_clients**](docs/WorkspacesApi.md#list_reseller_clients) | **GET** /{workspaceUuid}/clients | List client workspaces
*PostBoost::WorkspacesApi* | [**list_workspaces**](docs/WorkspacesApi.md#list_workspaces) | **GET** /panel/workspaces | List workspaces
*PostBoost::WorkspacesApi* | [**remove_user_from_workspace**](docs/WorkspacesApi.md#remove_user_from_workspace) | **DELETE** /panel/workspaces/{workspaceUuid}/users | Remove user from workspace
*PostBoost::WorkspacesApi* | [**update_workspace**](docs/WorkspacesApi.md#update_workspace) | **PUT** /panel/workspaces/{workspaceUuid} | Update workspace
*PostBoost::WorkspacesApi* | [**update_workspace_user**](docs/WorkspacesApi.md#update_workspace_user) | **PUT** /panel/workspaces/{workspaceUuid}/users | Update user role in workspace

---

## Links

- Docs and quick start: https://postboost.co/docs/quickstart
- API reference: https://postboost.co/docs/api
- MCP server for AI agents: https://postboost.co/docs/mcp
- All PostBoost open-source projects: https://github.com/postboost-co
- Awesome PostBoost: https://github.com/postboost-co/awesome-postboost

## Authentication

Create an API token in PostBoost under **Settings → Access Tokens** and pass it as a Bearer token. Never commit tokens; read them from an environment variable such as `POSTBOOST_API_TOKEN`.

## Contributing

This Ruby SDK is generated from the [PostBoost OpenAPI spec](https://postboost.co/docs/api). Bugs and feature requests: open an issue in [postboost-ruby](https://github.com/postboost-co/postboost-ruby/issues). Generated code is overwritten on every release, so fixes usually land in the spec or the generator templates; see [CONTRIBUTING.md](CONTRIBUTING.md).

Security issues: see [SECURITY.md](SECURITY.md). Questions: hi@postboost.co.

## License

MIT, see [LICENSE](LICENSE).

---

## Links

- Docs and quick start: https://postboost.co/docs/quickstart
- API reference: https://postboost.co/docs/api
- MCP server for AI agents: https://postboost.co/docs/mcp
- All PostBoost open-source projects: https://github.com/postboost-co
- Awesome PostBoost: https://github.com/postboost-co/awesome-postboost

## Authentication

Create an API token in PostBoost under **Settings → Access Tokens** and pass it as a Bearer token. Never commit tokens; read them from an environment variable such as `POSTBOOST_API_TOKEN`.

## Contributing

This Ruby SDK is generated from the [PostBoost OpenAPI spec](https://postboost.co/docs/api). Bugs and feature requests: open an issue in [postboost-ruby](https://github.com/postboost-co/postboost-ruby/issues). Generated code is overwritten on every release, so fixes usually land in the spec or the generator templates; see [CONTRIBUTING.md](CONTRIBUTING.md).

Security issues: see [SECURITY.md](SECURITY.md). Questions: hi@postboost.co.

## License

MIT, see [LICENSE](LICENSE).
