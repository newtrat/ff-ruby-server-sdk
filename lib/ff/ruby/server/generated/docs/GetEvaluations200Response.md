# OpenapiClient::GetEvaluations200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **version** | **Integer** | The version of this object.  The version will be incremented each time the object is modified | [optional] |
| **page_count** | **Integer** | The total number of pages |  |
| **item_count** | **Integer** | The total number of items |  |
| **page_size** | **Integer** | The number of items per page |  |
| **page_index** | **Integer** | The current page |  |

## Example

```ruby
require 'openapi_client'

instance = OpenapiClient::GetEvaluations200Response.new(
  version: 5,
  page_count: 100,
  item_count: 1,
  page_size: 1,
  page_index: 0
)
```

