# OpenapiClient::ProxyApi

All URIs are relative to *http://localhost/api/1.0*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**authenticate_proxy_key**](ProxyApi.md#authenticate_proxy_key) | **POST** /proxy/auth | Endpoint that the Proxy can use to authenticate with the client server |
| [**get_proxy_config**](ProxyApi.md#get_proxy_config) | **GET** /proxy/config | Gets Proxy config for multiple environments |


## authenticate_proxy_key

> <AuthenticationResponse> authenticate_proxy_key(opts)

Endpoint that the Proxy can use to authenticate with the client server

Endpoint that the Proxy can use to authenticate with the client server

### Examples

```ruby
require 'time'
require 'openapi_client'

api_instance = OpenapiClient::ProxyApi.new
opts = {
  authenticate_proxy_key_request: OpenapiClient::AuthenticateProxyKeyRequest.new({proxy_key: '896045f3-42ee-4e73-9154-086644768b96'}) # AuthenticateProxyKeyRequest | 
}

begin
  # Endpoint that the Proxy can use to authenticate with the client server
  result = api_instance.authenticate_proxy_key(opts)
  p result
rescue OpenapiClient::ApiError => e
  puts "Error when calling ProxyApi->authenticate_proxy_key: #{e}"
end
```

#### Using the authenticate_proxy_key_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AuthenticationResponse>, Integer, Hash)> authenticate_proxy_key_with_http_info(opts)

```ruby
begin
  # Endpoint that the Proxy can use to authenticate with the client server
  data, status_code, headers = api_instance.authenticate_proxy_key_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AuthenticationResponse>
rescue OpenapiClient::ApiError => e
  puts "Error when calling ProxyApi->authenticate_proxy_key_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **authenticate_proxy_key_request** | [**AuthenticateProxyKeyRequest**](AuthenticateProxyKeyRequest.md) |  | [optional] |

### Return type

[**AuthenticationResponse**](AuthenticationResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## get_proxy_config

> <ProxyConfig> get_proxy_config(key, opts)

Gets Proxy config for multiple environments

Gets Proxy config for multiple environments if the Key query param is provided or gets config for a single environment if an environment query param is provided

### Examples

```ruby
require 'time'
require 'openapi_client'
# setup authorization
OpenapiClient.configure do |config|
  # Configure Bearer authorization (JWT): BearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = OpenapiClient::ProxyApi.new
key = 'key_example' # String | Accpets a Proxy Key.
opts = {
  page_number: 56, # Integer | PageNumber
  page_size: 56, # Integer | PageSize
  cluster: 'cluster_example', # String | Unique identifier for the cluster for the account
  environment: 'environment_example' # String | Accepts an EnvironmentID. If this is provided then the endpoint will only return config for this environment. If this is left empty then the Proxy will return config for all environments associated with the Proxy Key.
}

begin
  # Gets Proxy config for multiple environments
  result = api_instance.get_proxy_config(key, opts)
  p result
rescue OpenapiClient::ApiError => e
  puts "Error when calling ProxyApi->get_proxy_config: #{e}"
end
```

#### Using the get_proxy_config_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ProxyConfig>, Integer, Hash)> get_proxy_config_with_http_info(key, opts)

```ruby
begin
  # Gets Proxy config for multiple environments
  data, status_code, headers = api_instance.get_proxy_config_with_http_info(key, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ProxyConfig>
rescue OpenapiClient::ApiError => e
  puts "Error when calling ProxyApi->get_proxy_config_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **key** | **String** | Accpets a Proxy Key. |  |
| **page_number** | **Integer** | PageNumber | [optional] |
| **page_size** | **Integer** | PageSize | [optional] |
| **cluster** | **String** | Unique identifier for the cluster for the account | [optional] |
| **environment** | **String** | Accepts an EnvironmentID. If this is provided then the endpoint will only return config for this environment. If this is left empty then the Proxy will return config for all environments associated with the Proxy Key. | [optional] |

### Return type

[**ProxyConfig**](ProxyConfig.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

