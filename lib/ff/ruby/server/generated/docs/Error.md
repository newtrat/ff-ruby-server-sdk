# OpenapiClient::Error

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **code** | **String** | The http error code |  |
| **message** | **String** | The reason the request failed |  |
| **details** | **Object** | Additional details about the error | [optional] |

## Example

```ruby
require 'openapi_client'

instance = OpenapiClient::Error.new(
  code: 404,
  message: Error retrieving projects, organization &#39;default_org&#39; does not exist,
  details: null
)
```

