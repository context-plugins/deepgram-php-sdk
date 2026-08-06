
# Error Response Modern Error

*This model accepts additional fields of type array.*

## Structure

`ErrorResponseModernError`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `category` | `?string` | Optional | The category of the error | getCategory(): ?string | setCategory(?string category): void |
| `message` | `?string` | Optional | A message about the error | getMessage(): ?string | setMessage(?string message): void |
| `details` | `?string` | Optional | A description of the error | getDetails(): ?string | setDetails(?string details): void |
| `requestId` | `?string` | Optional | The unique identifier of the request | getRequestId(): ?string | setRequestId(?string requestId): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\ErrorResponseModernErrorBuilder;
use DeepgramLib\ApiHelper;

$errorResponseModernError = ErrorResponseModernErrorBuilder::init()
    ->category('category6')
    ->message('message8')
    ->details('details8')
    ->requestId('request_id0')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

