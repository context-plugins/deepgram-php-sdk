
# Usage Breakdown V1 Response

*This model accepts additional fields of type array.*

## Structure

`UsageBreakdownV1Response`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `start` | `DateTime` | Required | Start date of the usage period | getStart(): \DateTime | setStart(\DateTime start): void |
| `end` | `DateTime` | Required | End date of the usage period | getEnd(): \DateTime | setEnd(\DateTime end): void |
| `resolution` | [`UsageBreakdownV1ResponseResolution`](../../doc/models/usage-breakdown-v1-response-resolution.md) | Required | - | getResolution(): UsageBreakdownV1ResponseResolution | setResolution(UsageBreakdownV1ResponseResolution resolution): void |
| `results` | [`UsageBreakdownV1ResponseResultsItems[]`](../../doc/models/usage-breakdown-v1-response-results-items.md) | Required | - | getResults(): array | setResults(array results): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\UsageBreakdownV1ResponseBuilder;
use DeepgramLib\Utils\DateTimeHelper;
use DeepgramLib\Models\Builders\UsageBreakdownV1ResponseResolutionBuilder;
use DeepgramLib\ApiHelper;
use DeepgramLib\Models\Builders\UsageBreakdownV1ResponseResultsItemsBuilder;
use DeepgramLib\Models\Builders\UsageBreakdownV1ResponseResultsItemsGroupingBuilder;

$usageBreakdownV1Response = UsageBreakdownV1ResponseBuilder::init(
    DateTimeHelper::fromSimpleDateRequired('2016-03-13'),
    DateTimeHelper::fromSimpleDateRequired('2016-03-13'),
    UsageBreakdownV1ResponseResolutionBuilder::init(
        'units8',
        98.28
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build(),
    [
        UsageBreakdownV1ResponseResultsItemsBuilder::init(
            127.36,
            195.94,
            198.56,
            251.3,
            96.28,
            224.32,
            144.02,
            UsageBreakdownV1ResponseResultsItemsGroupingBuilder::init()
                ->start(DateTimeHelper::fromSimpleDate('2016-03-13'))
                ->end(DateTimeHelper::fromSimpleDate('2016-03-13'))
                ->accessor('accessor6')
                ->endpoint('endpoint6')
                ->featureSet('feature_set2')
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

