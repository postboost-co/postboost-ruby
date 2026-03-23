# PostBoost::InitiateRemoteUpload200Response

## Class instance methods

### `openapi_one_of`

Returns the list of classes defined in oneOf.

#### Example

```ruby
require 'postboost'

PostBoost::InitiateRemoteUpload200Response.openapi_one_of
# =>
# [
#   :'InitiateRemoteUpload200ResponseOneOf',
#   :'Media'
# ]
```

### build

Find the appropriate object from the `openapi_one_of` list and casts the data into it.

#### Example

```ruby
require 'postboost'

PostBoost::InitiateRemoteUpload200Response.build(data)
# => #<InitiateRemoteUpload200ResponseOneOf:0x00007fdd4aab02a0>

PostBoost::InitiateRemoteUpload200Response.build(data_that_doesnt_match)
# => nil
```

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| **data** | **Mixed** | data to be matched against the list of oneOf items |

#### Return type

- `InitiateRemoteUpload200ResponseOneOf`
- `Media`
- `nil` (if no type matches)

