# OpenapiClient::Clause

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique ID for the clause | [optional] |
| **attribute** | **String** | The attribute to use in the clause.  This can be any target attribute |  |
| **op** | **String** | The type of operation such as equals, starts_with, contains |  |
| **values** | **Array&lt;String&gt;** | The values that are compared against the operator |  |
| **negate** | **Boolean** | Is the operation negated? |  |

## Example

```ruby
require 'openapi_client'

instance = OpenapiClient::Clause.new(
  id: 32434243,
  attribute: identifier,
  op: starts_with,
  values: null,
  negate: false
)
```

