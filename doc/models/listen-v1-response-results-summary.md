
# Listen V1 Response Results Summary

*This model accepts additional fields of type array.*

## Structure

`ListenV1ResponseResultsSummary`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `result` | `?string` | Optional | - | getResult(): ?string | setResult(?string result): void |
| `short` | `?string` | Optional | - | getShort(): ?string | setShort(?string short): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\ListenV1ResponseResultsSummaryBuilder;
use RestApiLib\ApiHelper;

$listenV1ResponseResultsSummary = ListenV1ResponseResultsSummaryBuilder::init()
    ->result('result2')
    ->short('short0')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

