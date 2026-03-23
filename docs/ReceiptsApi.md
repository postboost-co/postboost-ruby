# PostBoost::ReceiptsApi

All URIs are relative to *https://postboost.co/app/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_receipt**](ReceiptsApi.md#create_receipt) | **POST** /panel/receipts | Create receipt |
| [**delete_receipt**](ReceiptsApi.md#delete_receipt) | **DELETE** /panel/receipts/{receiptUuid} | Delete receipt |
| [**delete_receipts_bulk**](ReceiptsApi.md#delete_receipts_bulk) | **DELETE** /panel/receipts | Delete receipts (bulk) |
| [**get_receipt**](ReceiptsApi.md#get_receipt) | **GET** /panel/receipts/{receiptUuid} | Get receipt |
| [**list_receipts**](ReceiptsApi.md#list_receipts) | **GET** /panel/receipts | List receipts |
| [**update_receipt**](ReceiptsApi.md#update_receipt) | **PUT** /panel/receipts/{receiptUuid} | Update receipt |


## create_receipt

> <Receipt> create_receipt(receipt_input)

Create receipt

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::ReceiptsApi.new
receipt_input = PostBoost::ReceiptInput.new({workspace_uuid: 'workspace_uuid_example', transaction_id: 'transaction_id_example', invoice_number: 'invoice_number_example', amount: 3.56, tax: 3.56, currency: 'USD', paid_at: Date.today}) # ReceiptInput | 

begin
  # Create receipt
  result = api_instance.create_receipt(receipt_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling ReceiptsApi->create_receipt: #{e}"
end
```

#### Using the create_receipt_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Receipt>, Integer, Hash)> create_receipt_with_http_info(receipt_input)

```ruby
begin
  # Create receipt
  data, status_code, headers = api_instance.create_receipt_with_http_info(receipt_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Receipt>
rescue PostBoost::ApiError => e
  puts "Error when calling ReceiptsApi->create_receipt_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **receipt_input** | [**ReceiptInput**](ReceiptInput.md) |  |  |

### Return type

[**Receipt**](Receipt.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_receipt

> Object delete_receipt(receipt_uuid)

Delete receipt

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::ReceiptsApi.new
receipt_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the receipt.

begin
  # Delete receipt
  result = api_instance.delete_receipt(receipt_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling ReceiptsApi->delete_receipt: #{e}"
end
```

#### Using the delete_receipt_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> delete_receipt_with_http_info(receipt_uuid)

```ruby
begin
  # Delete receipt
  data, status_code, headers = api_instance.delete_receipt_with_http_info(receipt_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue PostBoost::ApiError => e
  puts "Error when calling ReceiptsApi->delete_receipt_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **receipt_uuid** | **String** | UUID of the receipt. |  |

### Return type

**Object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## delete_receipts_bulk

> Object delete_receipts_bulk(delete_receipts_bulk_request)

Delete receipts (bulk)

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::ReceiptsApi.new
delete_receipts_bulk_request = PostBoost::DeleteReceiptsBulkRequest.new({receipts: ['receipts_example']}) # DeleteReceiptsBulkRequest | 

begin
  # Delete receipts (bulk)
  result = api_instance.delete_receipts_bulk(delete_receipts_bulk_request)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling ReceiptsApi->delete_receipts_bulk: #{e}"
end
```

#### Using the delete_receipts_bulk_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> delete_receipts_bulk_with_http_info(delete_receipts_bulk_request)

```ruby
begin
  # Delete receipts (bulk)
  data, status_code, headers = api_instance.delete_receipts_bulk_with_http_info(delete_receipts_bulk_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue PostBoost::ApiError => e
  puts "Error when calling ReceiptsApi->delete_receipts_bulk_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **delete_receipts_bulk_request** | [**DeleteReceiptsBulkRequest**](DeleteReceiptsBulkRequest.md) |  |  |

### Return type

**Object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## get_receipt

> <Receipt> get_receipt(receipt_uuid)

Get receipt

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::ReceiptsApi.new
receipt_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the receipt.

begin
  # Get receipt
  result = api_instance.get_receipt(receipt_uuid)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling ReceiptsApi->get_receipt: #{e}"
end
```

#### Using the get_receipt_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Receipt>, Integer, Hash)> get_receipt_with_http_info(receipt_uuid)

```ruby
begin
  # Get receipt
  data, status_code, headers = api_instance.get_receipt_with_http_info(receipt_uuid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Receipt>
rescue PostBoost::ApiError => e
  puts "Error when calling ReceiptsApi->get_receipt_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **receipt_uuid** | **String** | UUID of the receipt. |  |

### Return type

[**Receipt**](Receipt.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_receipts

> <ListReceipts200Response> list_receipts(opts)

List receipts

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::ReceiptsApi.new
opts = {
  workspace_uuid: '38400000-8cf0-11bd-b23e-10b96e4ef00d', # String | 
  invoice_number: 'invoice_number_example' # String | 
}

begin
  # List receipts
  result = api_instance.list_receipts(opts)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling ReceiptsApi->list_receipts: #{e}"
end
```

#### Using the list_receipts_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListReceipts200Response>, Integer, Hash)> list_receipts_with_http_info(opts)

```ruby
begin
  # List receipts
  data, status_code, headers = api_instance.list_receipts_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListReceipts200Response>
rescue PostBoost::ApiError => e
  puts "Error when calling ReceiptsApi->list_receipts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_uuid** | **String** |  | [optional] |
| **invoice_number** | **String** |  | [optional] |

### Return type

[**ListReceipts200Response**](ListReceipts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_receipt

> Object update_receipt(receipt_uuid, receipt_update_input)

Update receipt

### Examples

```ruby
require 'time'
require 'postboost'
# setup authorization
PostBoost.configure do |config|
  # Configure Bearer authorization: bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = PostBoost::ReceiptsApi.new
receipt_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | UUID of the receipt.
receipt_update_input = PostBoost::ReceiptUpdateInput.new({transaction_id: 'transaction_id_example', invoice_number: 'invoice_number_example', amount: 3.56, currency: 'currency_example', paid_at: Date.today}) # ReceiptUpdateInput | 

begin
  # Update receipt
  result = api_instance.update_receipt(receipt_uuid, receipt_update_input)
  p result
rescue PostBoost::ApiError => e
  puts "Error when calling ReceiptsApi->update_receipt: #{e}"
end
```

#### Using the update_receipt_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> update_receipt_with_http_info(receipt_uuid, receipt_update_input)

```ruby
begin
  # Update receipt
  data, status_code, headers = api_instance.update_receipt_with_http_info(receipt_uuid, receipt_update_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue PostBoost::ApiError => e
  puts "Error when calling ReceiptsApi->update_receipt_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **receipt_uuid** | **String** | UUID of the receipt. |  |
| **receipt_update_input** | [**ReceiptUpdateInput**](ReceiptUpdateInput.md) |  |  |

### Return type

**Object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

