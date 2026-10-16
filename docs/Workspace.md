# PostBoost::Workspace

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **uuid** | **String** |  |  |
| **name** | **String** |  |  |
| **hex_color** | **String** | Deprecated. Workspaces no longer have a colour (workspaces now use &#x60;avatar&#x60;); the API returns the constant &#x60;4f46e5&#x60; so existing clients keep working. Will be removed in API v2. | [optional] |
| **avatar** | **String** | URL of the workspace avatar, or null when none is set. Supersedes &#x60;hex_color&#x60;. | [optional] |
| **owner** | [**User**](User.md) |  | [optional] |
| **access_status** | **String** |  |  |
| **created_at** | **String** | Display string in the configured timezone and clock: &#x60;M j, H:i&#x60; this year, &#x60;M j, Y, H:i&#x60; otherwise (12-hour setting: &#x60;h:ia&#x60;), not RFC 3339. |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::Workspace.new(
  uuid: null,
  name: null,
  hex_color: 4f46e5,
  avatar: null,
  owner: null,
  access_status: null,
  created_at: Oct 16, 14:05
)
```

