# PostBoost::ReportBrandingInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **display_name** | **String** | Name in the report header; default the workspace name. | [optional] |
| **primary_color** | **String** |  | [optional] |
| **footer_text** | **String** |  | [optional] |
| **show_powered_by** | **Boolean** | Show \&quot;Generated with PostBoost\&quot; in the footer. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::ReportBrandingInput.new(
  display_name: null,
  primary_color: null,
  footer_text: null,
  show_powered_by: null
)
```

