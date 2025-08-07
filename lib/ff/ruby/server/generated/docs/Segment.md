# OpenapiClient::Segment

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **identifier** | **String** | Unique identifier for the target group. |  |
| **name** | **String** | Name of the target group. |  |
| **environment** | **String** | The environment this target group belongs to | [optional] |
| **tags** | [**Array&lt;Tag&gt;**](Tag.md) | Tags for this target group | [optional] |
| **included** | [**Array&lt;Target&gt;**](Target.md) | A list of Targets who belong to this target group | [optional] |
| **excluded** | [**Array&lt;Target&gt;**](Target.md) | A list of Targets who are excluded from this target group | [optional] |
| **rules** | [**Array&lt;Clause&gt;**](Clause.md) |  | [optional] |
| **serving_rules** | [**Array&lt;GroupServingRule&gt;**](GroupServingRule.md) | An array of rules that can cause a user to be included in this segment. | [optional] |
| **created_at** | **Integer** | The data and time in milliseconds when the group was created | [optional] |
| **modified_at** | **Integer** | The data and time in milliseconds when the group was last modified | [optional] |
| **version** | **Integer** | The version of this group.  Each time it is modified the version is incremented | [optional] |

## Example

```ruby
require 'openapi_client'

instance = OpenapiClient::Segment.new(
  identifier: null,
  name: Beta Testers,
  environment: Production,
  tags: null,
  included: null,
  excluded: null,
  rules: null,
  serving_rules: null,
  created_at: null,
  modified_at: null,
  version: 1
)
```

