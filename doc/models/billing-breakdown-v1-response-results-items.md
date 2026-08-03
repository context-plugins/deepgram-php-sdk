
# Billing Breakdown V1 Response Results Items

*This model accepts additional fields of type array.*

## Structure

`BillingBreakdownV1ResponseResultsItems`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `dollars` | `float` | Required | USD cost of the billing for this grouping | getDollars(): float | setDollars(float dollars): void |
| `grouping` | [`BillingBreakdownV1ResponseResultsItemsGrouping`](../../doc/models/billing-breakdown-v1-response-results-items-grouping.md) | Required | - | getGrouping(): BillingBreakdownV1ResponseResultsItemsGrouping | setGrouping(BillingBreakdownV1ResponseResultsItemsGrouping grouping): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\BillingBreakdownV1ResponseResultsItemsBuilder;
use RestApiLib\Models\Builders\BillingBreakdownV1ResponseResultsItemsGroupingBuilder;
use RestApiLib\Utils\DateTimeHelper;
use RestApiLib\ApiHelper;

$billingBreakdownV1ResponseResultsItems = BillingBreakdownV1ResponseResultsItemsBuilder::init(
    151.78,
    BillingBreakdownV1ResponseResultsItemsGroupingBuilder::init()
        ->start(DateTimeHelper::fromSimpleDate('2016-03-13'))
        ->end(DateTimeHelper::fromSimpleDate('2016-03-13'))
        ->accessor('accessor6')
        ->deployment('deployment6')
        ->lineItem('line_item8')
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

