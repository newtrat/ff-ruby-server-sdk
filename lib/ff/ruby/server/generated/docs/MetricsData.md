# OpenapiClient::MetricsData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **timestamp** | **Integer** | time at when this data was recorded |  |
| **count** | **Integer** |  |  |
| **metrics_type** | **String** | This can be of type FeatureMetrics |  |
| **attributes** | [**Array&lt;KeyValue&gt;**](KeyValue.md) |  |  |

## Example

```ruby
require 'openapi_client'

instance = OpenapiClient::MetricsData.new(
  timestamp: 1608175465,
  count: null,
  metrics_type: null,
  attributes: null
)
```

