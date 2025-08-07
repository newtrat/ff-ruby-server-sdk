# OpenapiClient::VariationMap

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **variation** | **String** | The variation identifier |  |
| **targets** | [**Array&lt;TargetMap&gt;**](TargetMap.md) | A list of target mappings | [optional] |
| **target_segments** | **Array&lt;String&gt;** | A list of target groups (segments) | [optional] |

## Example

```ruby
require 'openapi_client'

instance = OpenapiClient::VariationMap.new(
  variation: off-variation,
  targets: null,
  target_segments: null
)
```

