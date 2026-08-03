
# Usage Breakdown V1 Response Resolution

*This model accepts additional fields of type array.*

## Structure

`UsageBreakdownV1ResponseResolution`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `units` | `string` | Required | Time unit for the resolution | getUnits(): string | setUnits(string units): void |
| `amount` | `float` | Required | Amount of units | getAmount(): float | setAmount(float amount): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\UsageBreakdownV1ResponseResolutionBuilder;
use RestApiLib\ApiHelper;

$usageBreakdownV1ResponseResolution = UsageBreakdownV1ResponseResolutionBuilder::init(
    'units4',
    64.9
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

