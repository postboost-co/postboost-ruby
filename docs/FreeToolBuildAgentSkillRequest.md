# PostBoost::FreeToolBuildAgentSkillRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **format** | **String** | skill_md (an Agent Skills SKILL.md), agents_md (AGENTS.md) or system_prompt. | [optional][default to &#39;skill_md&#39;] |
| **name** | **String** | The skill name, normalised to lowercase letters, digits and hyphens and cut to 64 characters. | [optional][default to &#39;postboost-social-media&#39;] |
| **brand** | **String** | The brand the agent works for; omitted when empty. | [optional][default to &#39;&#39;] |
| **tasks** | **Array&lt;String&gt;** | What the agent does; the output keeps this enum&#39;s order. | [optional] |
| **networks** | **Array&lt;String&gt;** | Networks to add character-limit rules for; none leaves the section out. | [optional] |
| **autonomy** | **String** | How much the agent may do without asking. | [optional][default to &#39;drafts_only&#39;] |
| **daily_cap** | **Integer** | Posts per day the agent may create; 0 adds no cap line. | [optional][default to 5] |
| **brand_voice** | **Boolean** | Read the workspace brand voice before writing captions. | [optional][default to true] |
| **connection** | **String** | connector (the OAuth MCP connector) or api_token (the advanced MCP server with an API key). | [optional][default to &#39;connector&#39;] |
| **rules** | **Array&lt;String&gt;** | Your own do&#39;s and don&#39;ts, one per item. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolBuildAgentSkillRequest.new(
  format: null,
  name: null,
  brand: null,
  tasks: null,
  networks: null,
  autonomy: null,
  daily_cap: null,
  brand_voice: null,
  connection: null,
  rules: null
)
```

