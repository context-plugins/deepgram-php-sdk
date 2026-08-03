
# Billing Breakdown V1 Response

*This model accepts additional fields of type array.*

## Structure

`BillingBreakdownV1Response`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `start` | `DateTime` | Required | Start date of the billing summmary period | getStart(): \DateTime | setStart(\DateTime start): void |
| `end` | `DateTime` | Required | End date of the billing summary period | getEnd(): \DateTime | setEnd(\DateTime end): void |
| `resolution` | [`BillingBreakdownV1ResponseResolution`](../../doc/models/billing-breakdown-v1-response-resolution.md) | Required | - | getResolution(): BillingBreakdownV1ResponseResolution | setResolution(BillingBreakdownV1ResponseResolution resolution): void |
| `results` | [`BillingBreakdownV1ResponseResultsItems[]`](../../doc/models/billing-breakdown-v1-response-results-items.md) | Required | - | getResults(): array | setResults(array results): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\BillingBreakdownV1ResponseBuilder;
use RestApiLib\Utils\DateTimeHelper;
use RestApiLib\Models\Builders\BillingBreakdownV1ResponseResolutionBuilder;
use RestApiLib\ApiHelper;
use RestApiLib\Models\Builders\BillingBreakdownV1ResponseResultsItemsBuilder;
use RestApiLib\Models\Builders\BillingBreakdownV1ResponseResultsItemsGroupingBuilder;

$billingBreakdownV1Response = BillingBreakdownV1ResponseBuilder::init(
    DateTimeHelper::fromSimpleDateRequired('2016-03-13'),
    DateTimeHelper::fromSimpleDateRequired('2016-03-13'),
    BillingBreakdownV1ResponseResolutionBuilder::init(
        'units8',
        98.28
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build(),
    [
        BillingBreakdownV1ResponseResultsItemsBuilder::init(
            41.68,
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
            ->build()
    ]
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

