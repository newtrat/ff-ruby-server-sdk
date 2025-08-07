# OpenapiClient::Distribution

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **bucket_by** | **String** | The attribute to use when distributing targets across buckets |  |
| **variations** | [**Array&lt;WeightedVariation&gt;**](WeightedVariation.md) | A list of variations and the weight that should be given to each |  |

## Example

```ruby
require 'openapi_client'

instance = OpenapiClient::Distribution.new(
  bucket_by: null,
  variations: null
)
```

