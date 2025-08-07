# OpenapiClient::ProxyConfigAllOfEnvironments

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  | [optional] |
| **api_keys** | **Array&lt;String&gt;** |  | [optional] |
| **feature_configs** | [**Array&lt;FeatureConfig&gt;**](FeatureConfig.md) |  | [optional] |
| **segments** | [**Array&lt;Segment&gt;**](Segment.md) |  | [optional] |

## Example

```ruby
require 'openapi_client'

instance = OpenapiClient::ProxyConfigAllOfEnvironments.new(
  id: null,
  api_keys: null,
  feature_configs: null,
  segments: null
)
```

