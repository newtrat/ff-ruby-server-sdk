# OpenapiClient::FeatureConfig

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **project** | **String** |  |  |
| **environment** | **String** |  |  |
| **feature** | **String** |  |  |
| **state** | [**FeatureState**](FeatureState.md) |  |  |
| **kind** | **String** |  |  |
| **variations** | [**Array&lt;Variation&gt;**](Variation.md) |  |  |
| **rules** | [**Array&lt;ServingRule&gt;**](ServingRule.md) |  | [optional] |
| **default_serve** | [**Serve**](Serve.md) |  |  |
| **off_variation** | **String** |  |  |
| **prerequisites** | [**Array&lt;Prerequisite&gt;**](Prerequisite.md) |  | [optional] |
| **variation_to_target_map** | [**Array&lt;VariationMap&gt;**](VariationMap.md) |  | [optional] |
| **version** | **Integer** |  | [optional] |

## Example

```ruby
require 'openapi_client'

instance = OpenapiClient::FeatureConfig.new(
  project: null,
  environment: null,
  feature: null,
  state: null,
  kind: null,
  variations: null,
  rules: null,
  default_serve: null,
  off_variation: null,
  prerequisites: null,
  variation_to_target_map: null,
  version: null
)
```

