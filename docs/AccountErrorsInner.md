# PostBoost::AccountErrorsInner

## Class instance methods

### `openapi_one_of`

Returns the list of classes defined in oneOf.

#### Example

```ruby
require 'postboost'

PostBoost::AccountErrorsInner.openapi_one_of
# =>
# [
#   :'AccountErrorsInnerOneOf',
#   :'String'
# ]
```

### build

Find the appropriate object from the `openapi_one_of` list and casts the data into it.

#### Example

```ruby
require 'postboost'

PostBoost::AccountErrorsInner.build(data)
# => #<AccountErrorsInnerOneOf:0x00007fdd4aab02a0>

PostBoost::AccountErrorsInner.build(data_that_doesnt_match)
# => nil
```

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| **data** | **Mixed** | data to be matched against the list of oneOf items |

#### Return type

- `AccountErrorsInnerOneOf`
- `String`
- `nil` (if no type matches)

