
# Error Response Legacy Error

*This model accepts additional fields of type array.*

## Structure

`ErrorResponseLegacyError`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `errCode` | `?string` | Optional | The error code | getErrCode(): ?string | setErrCode(?string errCode): void |
| `errMsg` | `?string` | Optional | The error message | getErrMsg(): ?string | setErrMsg(?string errMsg): void |
| `requestId` | `?string` | Optional | The request ID | getRequestId(): ?string | setRequestId(?string requestId): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\ErrorResponseLegacyErrorBuilder;
use RestApiLib\ApiHelper;

$errorResponseLegacyError = ErrorResponseLegacyErrorBuilder::init()
    ->errCode('err_code8')
    ->errMsg('err_msg0')
    ->requestId('request_id8')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

