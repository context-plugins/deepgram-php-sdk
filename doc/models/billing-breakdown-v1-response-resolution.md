
# Billing Breakdown V1 Response Resolution

*This model accepts additional fields of type array.*

## Structure

`BillingBreakdownV1ResponseResolution`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `units` | `string` | Required | Time unit for the resolution | getUnits(): string | setUnits(string units): void |
| `amount` | `float` | Required | Amount of units | getAmount(): float | setAmount(float amount): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\BillingBreakdownV1ResponseResolutionBuilder;
use RestApiLib\ApiHelper;

$billingBreakdownV1ResponseResolution = BillingBreakdownV1ResponseResolutionBuilder::init(
    'units2',
    230.54
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

