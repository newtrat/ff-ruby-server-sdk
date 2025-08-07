# OpenapiClient::MetricsApi

All URIs are relative to *http://localhost/api/1.0*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**post_metrics**](MetricsApi.md#post_metrics) | **POST** /metrics/{environmentUUID} | Send metrics to the Analytics server. |


## post_metrics

> post_metrics(environment_uuid, opts)

Send metrics to the Analytics server.

Send metrics to Analytics server

### Examples

```ruby
require 'time'
require 'openapi_client'
# setup authorization
OpenapiClient.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['api-key'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['api-key'] = 'Bearer'

  # Configure Bearer authorization (JWT): BearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = OpenapiClient::MetricsApi.new
environment_uuid = 'environment_uuid_example' # String | environment parameter in query.
opts = {
  cluster: 'cluster_example', # String | Unique identifier for the cluster for the account
  metrics: OpenapiClient::Metrics.new # Metrics | 
}

begin
  # Send metrics to the Analytics server.
  api_instance.post_metrics(environment_uuid, opts)
rescue OpenapiClient::ApiError => e
  puts "Error when calling MetricsApi->post_metrics: #{e}"
end
```

#### Using the post_metrics_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> post_metrics_with_http_info(environment_uuid, opts)

```ruby
begin
  # Send metrics to the Analytics server.
  data, status_code, headers = api_instance.post_metrics_with_http_info(environment_uuid, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue OpenapiClient::ApiError => e
  puts "Error when calling MetricsApi->post_metrics_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **environment_uuid** | **String** | environment parameter in query. |  |
| **cluster** | **String** | Unique identifier for the cluster for the account | [optional] |
| **metrics** | [**Metrics**](Metrics.md) |  | [optional] |

### Return type

nil (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

