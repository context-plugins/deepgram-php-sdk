
# Usage V1 Response Resolution

*This model accepts additional fields of type array.*

## Structure

`UsageV1ResponseResolution`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `units` | `?string` | Optional | - | getUnits(): ?string | setUnits(?string units): void |
| `amount` | `?float` | Optional | - | getAmount(): ?float | setAmount(?float amount): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\UsageV1ResponseResolutionBuilder;
use RestApiLib\ApiHelper;

$usageV1ResponseResolution = UsageV1ResponseResolutionBuilder::init()
    ->units('units8')
    ->amount(114.68)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

