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
| **Version** | v1.3.0 |

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
*PostBoost::AccountsApi* | [**get_account**](docs/AccountsApi.md#get_account) | **GET** /{workspaceUuid}/accounts/{accountUuid} | Get account
*PostBoost::AccountsApi* | [**list_accounts**](docs/AccountsApi.md#list_accounts) | **GET** /{workspaceUuid}/accounts | List accounts
*PostBoost::MediaApi* | [**abort_chunked_upload**](docs/MediaApi.md#abort_chunked_upload) | **DELETE** /{workspaceUuid}/media/chunked/{uploadUuid} | Abort chunked upload
*PostBoost::MediaApi* | [**complete_chunked_upload**](docs/MediaApi.md#complete_chunked_upload) | **POST** /{workspaceUuid}/media/chunked/{uploadUuid}/complete | Complete chunked upload
*PostBoost::MediaApi* | [**delete_media_bulk**](docs/MediaApi.md#delete_media_bulk) | **DELETE** /{workspaceUuid}/media | Delete media (bulk)
*PostBoost::MediaApi* | [**get_media**](docs/MediaApi.md#get_media) | **GET** /{workspaceUuid}/media/{mediaUuid} | Get media
*PostBoost::MediaApi* | [**get_remote_upload_status**](docs/MediaApi.md#get_remote_upload_status) | **GET** /{workspaceUuid}/media/remote/{downloadId}/status | Get remote upload status
*PostBoost::MediaApi* | [**initiate_chunked_upload**](docs/MediaApi.md#initiate_chunked_upload) | **POST** /{workspaceUuid}/media/chunked/initiate | Initiate chunked upload
*PostBoost::MediaApi* | [**initiate_remote_upload**](docs/MediaApi.md#initiate_remote_upload) | **POST** /{workspaceUuid}/media/remote/initiate | Initiate remote upload
*PostBoost::MediaApi* | [**list_media**](docs/MediaApi.md#list_media) | **GET** /{workspaceUuid}/media | List media
*PostBoost::MediaApi* | [**update_media**](docs/MediaApi.md#update_media) | **PUT** /{workspaceUuid}/media/{mediaUuid} | Update media
*PostBoost::MediaApi* | [**upload_chunk**](docs/MediaApi.md#upload_chunk) | **POST** /{workspaceUuid}/media/chunked/{uploadUuid}/upload | Upload a chunk
*PostBoost::MediaApi* | [**upload_media**](docs/MediaApi.md#upload_media) | **POST** /{workspaceUuid}/media | Upload media (binary)
*PostBoost::PostsApi* | [**add_post_to_queue**](docs/PostsApi.md#add_post_to_queue) | **POST** /{workspaceUuid}/posts/add-to-queue/{postUuid} | Add post to queue
*PostBoost::PostsApi* | [**approve_post**](docs/PostsApi.md#approve_post) | **POST** /{workspaceUuid}/posts/approve/{postUuid} | Approve post
*PostBoost::PostsApi* | [**create_post**](docs/PostsApi.md#create_post) | **POST** /{workspaceUuid}/posts | Create post
*PostBoost::PostsApi* | [**delete_post**](docs/PostsApi.md#delete_post) | **DELETE** /{workspaceUuid}/posts/{postUuid} | Delete post
*PostBoost::PostsApi* | [**delete_posts_bulk**](docs/PostsApi.md#delete_posts_bulk) | **DELETE** /{workspaceUuid}/posts | Delete posts (bulk)
*PostBoost::PostsApi* | [**get_post**](docs/PostsApi.md#get_post) | **GET** /{workspaceUuid}/posts/{postUuid} | Get post
*PostBoost::PostsApi* | [**list_posts**](docs/PostsApi.md#list_posts) | **GET** /{workspaceUuid}/posts | List posts
*PostBoost::PostsApi* | [**schedule_post**](docs/PostsApi.md#schedule_post) | **POST** /{workspaceUuid}/posts/schedule/{postUuid} | Schedule post
*PostBoost::PostsApi* | [**update_post**](docs/PostsApi.md#update_post) | **PUT** /{workspaceUuid}/posts/{postUuid} | Update post
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
*PostBoost::UsersApi* | [**create_user**](docs/UsersApi.md#create_user) | **POST** /panel/users | Create user
*PostBoost::UsersApi* | [**delete_user**](docs/UsersApi.md#delete_user) | **DELETE** /panel/users/{userId} | Delete user
*PostBoost::UsersApi* | [**delete_users_bulk**](docs/UsersApi.md#delete_users_bulk) | **DELETE** /panel/users | Delete users (bulk)
*PostBoost::UsersApi* | [**get_user**](docs/UsersApi.md#get_user) | **GET** /panel/users/{userId} | Get user
*PostBoost::UsersApi* | [**list_users**](docs/UsersApi.md#list_users) | **GET** /panel/users | List users
*PostBoost::UsersApi* | [**update_user**](docs/UsersApi.md#update_user) | **PUT** /panel/users/{userId} | Update user
*PostBoost::WorkspacesApi* | [**add_user_to_workspace**](docs/WorkspacesApi.md#add_user_to_workspace) | **POST** /panel/workspaces/{workspaceUuid}/users | Add user to workspace
*PostBoost::WorkspacesApi* | [**create_workspace**](docs/WorkspacesApi.md#create_workspace) | **POST** /panel/workspaces | Create workspace
*PostBoost::WorkspacesApi* | [**delete_workspace**](docs/WorkspacesApi.md#delete_workspace) | **DELETE** /panel/workspaces/{workspaceUuid} | Delete workspace
*PostBoost::WorkspacesApi* | [**delete_workspaces_bulk**](docs/WorkspacesApi.md#delete_workspaces_bulk) | **DELETE** /panel/workspaces | Delete workspaces (bulk)
*PostBoost::WorkspacesApi* | [**get_workspace**](docs/WorkspacesApi.md#get_workspace) | **GET** /panel/workspaces/{workspaceUuid} | Get workspace
*PostBoost::WorkspacesApi* | [**list_workspaces**](docs/WorkspacesApi.md#list_workspaces) | **GET** /panel/workspaces | List workspaces
*PostBoost::WorkspacesApi* | [**remove_user_from_workspace**](docs/WorkspacesApi.md#remove_user_from_workspace) | **DELETE** /panel/workspaces/{workspaceUuid}/users | Remove user from workspace
*PostBoost::WorkspacesApi* | [**update_workspace**](docs/WorkspacesApi.md#update_workspace) | **PUT** /panel/workspaces/{workspaceUuid} | Update workspace
*PostBoost::WorkspacesApi* | [**update_workspace_user**](docs/WorkspacesApi.md#update_workspace_user) | **PUT** /panel/workspaces/{workspaceUuid}/users | Update user role in workspace
