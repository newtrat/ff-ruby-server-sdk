# OpenapiClient::ClientApi

All URIs are relative to *http://localhost/api/1.0*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**authenticate**](ClientApi.md#authenticate) | **POST** /client/auth | Authenticate with the admin server. |
| [**get_all_segments**](ClientApi.md#get_all_segments) | **GET** /client/env/{environmentUUID}/target-segments | Retrieve all segments. |
| [**get_evaluation_by_identifier**](ClientApi.md#get_evaluation_by_identifier) | **GET** /client/env/{environmentUUID}/target/{target}/evaluations/{feature} | Get feature evaluations for target |
| [**get_evaluations**](ClientApi.md#get_evaluations) | **GET** /client/env/{environmentUUID}/target/{target}/evaluations | Get feature evaluations for target |
| [**get_feature_config**](ClientApi.md#get_feature_config) | **GET** /client/env/{environmentUUID}/feature-configs | Get all feature flags activations |
| [**get_feature_config_by_identifier**](ClientApi.md#get_feature_config_by_identifier) | **GET** /client/env/{environmentUUID}/feature-configs/{identifier} | Get feature config |
| [**get_segment_by_identifier**](ClientApi.md#get_segment_by_identifier) | **GET** /client/env/{environmentUUID}/target-segments/{identifier} | Retrieve a segment by identifier |
| [**stream**](ClientApi.md#stream) | **GET** /stream | Stream endpoint. |


## authenticate

> <AuthenticationResponse> authenticate(opts)

Authenticate with the admin server.

Used to retrieve all target segments for certain account id.

### Examples

```ruby
require 'time'
require 'openapi_client'

api_instance = OpenapiClient::ClientApi.new
opts = {
  authentication_request: OpenapiClient::AuthenticationRequest.new({api_key: '896045f3-42ee-4e73-9154-086644768b96'}) # AuthenticationRequest | 
}

begin
  # Authenticate with the admin server.
  result = api_instance.authenticate(opts)
  p result
rescue OpenapiClient::ApiError => e
  puts "Error when calling ClientApi->authenticate: #{e}"
end
```

#### Using the authenticate_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AuthenticationResponse>, Integer, Hash)> authenticate_with_http_info(opts)

```ruby
begin
  # Authenticate with the admin server.
  data, status_code, headers = api_instance.authenticate_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AuthenticationResponse>
rescue OpenapiClient::ApiError => e
  puts "Error when calling ClientApi->authenticate_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **authentication_request** | [**AuthenticationRequest**](AuthenticationRequest.md) |  | [optional] |

### Return type

[**AuthenticationResponse**](AuthenticationResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## get_all_segments

> <Array<Segment>> get_all_segments(environment_uuid, opts)

Retrieve all segments.

Used to retrieve all segments for certain account id.

### Examples

```ruby
require 'time'
require 'openapi_client'
# setup authorization
OpenapiClient.configure do |config|
  # Configure Bearer authorization (JWT): BearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = OpenapiClient::ClientApi.new
environment_uuid = 'environment_uuid_example' # String | Unique identifier for the environment object in the API.
opts = {
  cluster: 'cluster_example', # String | Unique identifier for the cluster for the account
  rules: 'rules_example' # String | When set to rules=v2 will return AND rule compatible serving_rules field. When not set or set to any other value will return old rules field only compatible with OR rules.
}

begin
  # Retrieve all segments.
  result = api_instance.get_all_segments(environment_uuid, opts)
  p result
rescue OpenapiClient::ApiError => e
  puts "Error when calling ClientApi->get_all_segments: #{e}"
end
```

#### Using the get_all_segments_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Segment>>, Integer, Hash)> get_all_segments_with_http_info(environment_uuid, opts)

```ruby
begin
  # Retrieve all segments.
  data, status_code, headers = api_instance.get_all_segments_with_http_info(environment_uuid, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Segment>>
rescue OpenapiClient::ApiError => e
  puts "Error when calling ClientApi->get_all_segments_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **environment_uuid** | **String** | Unique identifier for the environment object in the API. |  |
| **cluster** | **String** | Unique identifier for the cluster for the account | [optional] |
| **rules** | **String** | When set to rules&#x3D;v2 will return AND rule compatible serving_rules field. When not set or set to any other value will return old rules field only compatible with OR rules. | [optional] |

### Return type

[**Array&lt;Segment&gt;**](Segment.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_evaluation_by_identifier

> <Evaluation> get_evaluation_by_identifier(environment_uuid, feature, target, opts)

Get feature evaluations for target

### Examples

```ruby
require 'time'
require 'openapi_client'
# setup authorization
OpenapiClient.configure do |config|
  # Configure Bearer authorization (JWT): BearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = OpenapiClient::ClientApi.new
environment_uuid = 'environment_uuid_example' # String | Unique identifier for the environment object in the API.
feature = 'feature_example' # String | Unique identifier for the flag object in the API.
target = 'target_example' # String | Unique identifier for the target object in the API.
opts = {
  cluster: 'cluster_example' # String | Unique identifier for the cluster for the account
}

begin
  # Get feature evaluations for target
  result = api_instance.get_evaluation_by_identifier(environment_uuid, feature, target, opts)
  p result
rescue OpenapiClient::ApiError => e
  puts "Error when calling ClientApi->get_evaluation_by_identifier: #{e}"
end
```

#### Using the get_evaluation_by_identifier_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Evaluation>, Integer, Hash)> get_evaluation_by_identifier_with_http_info(environment_uuid, feature, target, opts)

```ruby
begin
  # Get feature evaluations for target
  data, status_code, headers = api_instance.get_evaluation_by_identifier_with_http_info(environment_uuid, feature, target, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Evaluation>
rescue OpenapiClient::ApiError => e
  puts "Error when calling ClientApi->get_evaluation_by_identifier_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **environment_uuid** | **String** | Unique identifier for the environment object in the API. |  |
| **feature** | **String** | Unique identifier for the flag object in the API. |  |
| **target** | **String** | Unique identifier for the target object in the API. |  |
| **cluster** | **String** | Unique identifier for the cluster for the account | [optional] |

### Return type

[**Evaluation**](Evaluation.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_evaluations

> <GetEvaluations200Response> get_evaluations(environment_uuid, target, opts)

Get feature evaluations for target

### Examples

```ruby
require 'time'
require 'openapi_client'
# setup authorization
OpenapiClient.configure do |config|
  # Configure Bearer authorization (JWT): BearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = OpenapiClient::ClientApi.new
environment_uuid = 'environment_uuid_example' # String | Unique identifier for the environment object in the API.
target = 'target_example' # String | Unique identifier for the target object in the API.
opts = {
  cluster: 'cluster_example' # String | Unique identifier for the cluster for the account
}

begin
  # Get feature evaluations for target
  result = api_instance.get_evaluations(environment_uuid, target, opts)
  p result
rescue OpenapiClient::ApiError => e
  puts "Error when calling ClientApi->get_evaluations: #{e}"
end
```

#### Using the get_evaluations_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetEvaluations200Response>, Integer, Hash)> get_evaluations_with_http_info(environment_uuid, target, opts)

```ruby
begin
  # Get feature evaluations for target
  data, status_code, headers = api_instance.get_evaluations_with_http_info(environment_uuid, target, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetEvaluations200Response>
rescue OpenapiClient::ApiError => e
  puts "Error when calling ClientApi->get_evaluations_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **environment_uuid** | **String** | Unique identifier for the environment object in the API. |  |
| **target** | **String** | Unique identifier for the target object in the API. |  |
| **cluster** | **String** | Unique identifier for the cluster for the account | [optional] |

### Return type

[**GetEvaluations200Response**](GetEvaluations200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_feature_config

> <Array<FeatureConfig>> get_feature_config(environment_uuid, opts)

Get all feature flags activations

All feature flags with activations in project environment

### Examples

```ruby
require 'time'
require 'openapi_client'
# setup authorization
OpenapiClient.configure do |config|
  # Configure Bearer authorization (JWT): BearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = OpenapiClient::ClientApi.new
environment_uuid = 'environment_uuid_example' # String | Unique identifier for the environment object in the API.
opts = {
  cluster: 'cluster_example' # String | Unique identifier for the cluster for the account
}

begin
  # Get all feature flags activations
  result = api_instance.get_feature_config(environment_uuid, opts)
  p result
rescue OpenapiClient::ApiError => e
  puts "Error when calling ClientApi->get_feature_config: #{e}"
end
```

#### Using the get_feature_config_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<FeatureConfig>>, Integer, Hash)> get_feature_config_with_http_info(environment_uuid, opts)

```ruby
begin
  # Get all feature flags activations
  data, status_code, headers = api_instance.get_feature_config_with_http_info(environment_uuid, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<FeatureConfig>>
rescue OpenapiClient::ApiError => e
  puts "Error when calling ClientApi->get_feature_config_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **environment_uuid** | **String** | Unique identifier for the environment object in the API. |  |
| **cluster** | **String** | Unique identifier for the cluster for the account | [optional] |

### Return type

[**Array&lt;FeatureConfig&gt;**](FeatureConfig.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_feature_config_by_identifier

> <FeatureConfig> get_feature_config_by_identifier(identifier, environment_uuid, opts)

Get feature config

### Examples

```ruby
require 'time'
require 'openapi_client'
# setup authorization
OpenapiClient.configure do |config|
  # Configure Bearer authorization (JWT): BearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = OpenapiClient::ClientApi.new
identifier = 'identifier_example' # String | Unique identifier for the flag object in the API.
environment_uuid = 'environment_uuid_example' # String | Unique identifier for the environment object in the API.
opts = {
  cluster: 'cluster_example' # String | Unique identifier for the cluster for the account
}

begin
  # Get feature config
  result = api_instance.get_feature_config_by_identifier(identifier, environment_uuid, opts)
  p result
rescue OpenapiClient::ApiError => e
  puts "Error when calling ClientApi->get_feature_config_by_identifier: #{e}"
end
```

#### Using the get_feature_config_by_identifier_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FeatureConfig>, Integer, Hash)> get_feature_config_by_identifier_with_http_info(identifier, environment_uuid, opts)

```ruby
begin
  # Get feature config
  data, status_code, headers = api_instance.get_feature_config_by_identifier_with_http_info(identifier, environment_uuid, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FeatureConfig>
rescue OpenapiClient::ApiError => e
  puts "Error when calling ClientApi->get_feature_config_by_identifier_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **identifier** | **String** | Unique identifier for the flag object in the API. |  |
| **environment_uuid** | **String** | Unique identifier for the environment object in the API. |  |
| **cluster** | **String** | Unique identifier for the cluster for the account | [optional] |

### Return type

[**FeatureConfig**](FeatureConfig.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_segment_by_identifier

> <Segment> get_segment_by_identifier(identifier, environment_uuid, opts)

Retrieve a segment by identifier

Used to retrieve a segment for a certain account id by identifier

### Examples

```ruby
require 'time'
require 'openapi_client'
# setup authorization
OpenapiClient.configure do |config|
  # Configure Bearer authorization (JWT): BearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = OpenapiClient::ClientApi.new
identifier = 'identifier_example' # String | Unique identifier for the segment object in the API
environment_uuid = 'environment_uuid_example' # String | Unique identifier for the environment object in the API
opts = {
  cluster: 'cluster_example', # String | Unique identifier for the cluster for the account
  rules: 'rules_example' # String | When set to rules=v2 will return AND rule compatible serving_rules field. When not set or set to any other value will return old rules field only compatible with OR rules.
}

begin
  # Retrieve a segment by identifier
  result = api_instance.get_segment_by_identifier(identifier, environment_uuid, opts)
  p result
rescue OpenapiClient::ApiError => e
  puts "Error when calling ClientApi->get_segment_by_identifier: #{e}"
end
```

#### Using the get_segment_by_identifier_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Segment>, Integer, Hash)> get_segment_by_identifier_with_http_info(identifier, environment_uuid, opts)

```ruby
begin
  # Retrieve a segment by identifier
  data, status_code, headers = api_instance.get_segment_by_identifier_with_http_info(identifier, environment_uuid, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Segment>
rescue OpenapiClient::ApiError => e
  puts "Error when calling ClientApi->get_segment_by_identifier_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **identifier** | **String** | Unique identifier for the segment object in the API |  |
| **environment_uuid** | **String** | Unique identifier for the environment object in the API |  |
| **cluster** | **String** | Unique identifier for the cluster for the account | [optional] |
| **rules** | **String** | When set to rules&#x3D;v2 will return AND rule compatible serving_rules field. When not set or set to any other value will return old rules field only compatible with OR rules. | [optional] |

### Return type

[**Segment**](Segment.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## stream

> stream(api_key, opts)

Stream endpoint.

### Examples

```ruby
require 'time'
require 'openapi_client'
# setup authorization
OpenapiClient.configure do |config|
  # Configure Bearer authorization (JWT): BearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = OpenapiClient::ClientApi.new
api_key = 'api_key_example' # String | 
opts = {
  cluster: 'cluster_example' # String | Unique identifier for the cluster for the account
}

begin
  # Stream endpoint.
  api_instance.stream(api_key, opts)
rescue OpenapiClient::ApiError => e
  puts "Error when calling ClientApi->stream: #{e}"
end
```

#### Using the stream_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> stream_with_http_info(api_key, opts)

```ruby
begin
  # Stream endpoint.
  data, status_code, headers = api_instance.stream_with_http_info(api_key, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue OpenapiClient::ApiError => e
  puts "Error when calling ClientApi->stream_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **api_key** | **String** |  |  |
| **cluster** | **String** | Unique identifier for the cluster for the account | [optional] |

### Return type

nil (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

