# OpenapiClient::Target

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **identifier** | **String** | The unique identifier for this target |  |
| **account** | **String** | The account ID that the target belongs to |  |
| **org** | **String** | The identifier for the organization that the target belongs to |  |
| **environment** | **String** | The identifier for the environment that the target belongs to |  |
| **project** | **String** | The identifier for the project that this target belongs to |  |
| **name** | **String** | The name of this Target |  |
| **anonymous** | **Boolean** | Indicates if this target is anonymous | [optional] |
| **attributes** | **Object** | a JSON representation of the attributes for this target | [optional] |
| **created_at** | **Integer** | The date and time in milliseconds when this Target was created | [optional] |
| **segments** | [**Array&lt;Segment&gt;**](Segment.md) | A list of Target Groups (Segments) that this Target belongs to | [optional] |

## Example

```ruby
require 'openapi_client'

instance = OpenapiClient::Target.new(
  identifier: john-doe,
  account: abcXDdffdaffd,
  org: null,
  environment: null,
  project: null,
  name: John Doe,
  anonymous: null,
  attributes: {&quot;age&quot;:20,&quot;location&quot;:&quot;Belfast&quot;},
  created_at: null,
  segments: null
)
```

