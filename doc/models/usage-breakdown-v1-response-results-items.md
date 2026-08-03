
# Usage Breakdown V1 Response Results Items

*This model accepts additional fields of type array.*

## Structure

`UsageBreakdownV1ResponseResultsItems`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `hours` | `float` | Required | Audio hours processed | getHours(): float | setHours(float hours): void |
| `totalHours` | `float` | Required | Total hours including all processing | getTotalHours(): float | setTotalHours(float totalHours): void |
| `agentHours` | `float` | Required | Agent hours used | getAgentHours(): float | setAgentHours(float agentHours): void |
| `tokensIn` | `float` | Required | Number of input tokens | getTokensIn(): float | setTokensIn(float tokensIn): void |
| `tokensOut` | `float` | Required | Number of output tokens | getTokensOut(): float | setTokensOut(float tokensOut): void |
| `ttsCharacters` | `float` | Required | Number of text-to-speech characters processed | getTtsCharacters(): float | setTtsCharacters(float ttsCharacters): void |
| `requests` | `float` | Required | Number of requests | getRequests(): float | setRequests(float requests): void |
| `grouping` | [`UsageBreakdownV1ResponseResultsItemsGrouping`](../../doc/models/usage-breakdown-v1-response-results-items-grouping.md) | Required | - | getGrouping(): UsageBreakdownV1ResponseResultsItemsGrouping | setGrouping(UsageBreakdownV1ResponseResultsItemsGrouping grouping): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\UsageBreakdownV1ResponseResultsItemsBuilder;
use RestApiLib\Models\Builders\UsageBreakdownV1ResponseResultsItemsGroupingBuilder;
use RestApiLib\Utils\DateTimeHelper;
use RestApiLib\ApiHelper;

$usageBreakdownV1ResponseResultsItems = UsageBreakdownV1ResponseResultsItemsBuilder::init(
    49.58,
    116.88,
    119.5,
    172.24,
    17.22,
    145.26,
    32.92,
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
    ->build();
```

