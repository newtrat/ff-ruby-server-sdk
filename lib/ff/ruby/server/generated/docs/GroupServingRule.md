# OpenapiClient::GroupServingRule

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **rule_id** | **String** | The unique identifier for this rule |  |
| **priority** | **Integer** | The rules priority relative to other rules.  The rules are evaluated in order with 1 being the highest |  |
| **clauses** | [**Array&lt;Clause&gt;**](Clause.md) | A list of clauses to use in the rule |  |

## Example

```ruby
require 'openapi_client'

instance = OpenapiClient::GroupServingRule.new(
  rule_id: null,
  priority: 1,
  clauses: null
)
```

