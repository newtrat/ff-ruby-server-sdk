# OpenapiClient::Variation

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **identifier** | **String** | The unique identifier for the variation |  |
| **value** | **String** | The variation value to serve such as true or false for a boolean flag |  |
| **name** | **String** | The user friendly name of the variation | [optional] |
| **description** | **String** | A description of the variation | [optional] |

## Example

```ruby
require 'openapi_client'

instance = OpenapiClient::Variation.new(
  identifier: off-variation,
  value: true,
  name: Off VAriation,
  description: null
)
```

