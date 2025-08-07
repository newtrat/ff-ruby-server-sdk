# OpenapiClient::WeightedVariation

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **variation** | **String** | The variation identifier |  |
| **weight** | **Integer** | The weight to be given to the variation in percent |  |

## Example

```ruby
require 'openapi_client'

instance = OpenapiClient::WeightedVariation.new(
  variation: off-variation,
  weight: 50
)
```

