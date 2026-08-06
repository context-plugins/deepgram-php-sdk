
# Usage Breakdown V1 Response Results Items Grouping

*This model accepts additional fields of type array.*

## Structure

`UsageBreakdownV1ResponseResultsItemsGrouping`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `start` | `?DateTime` | Optional | Start date for this group | getStart(): ?\DateTime | setStart(?\DateTime start): void |
| `end` | `?DateTime` | Optional | End date for this group | getEnd(): ?\DateTime | setEnd(?\DateTime end): void |
| `accessor` | `?string` | Optional | Optional accessor identifier | getAccessor(): ?string | setAccessor(?string accessor): void |
| `endpoint` | `?string` | Optional | Optional endpoint identifier | getEndpoint(): ?string | setEndpoint(?string endpoint): void |
| `featureSet` | `?string` | Optional | Optional feature set identifier | getFeatureSet(): ?string | setFeatureSet(?string featureSet): void |
| `models` | `?(string[])` | Optional | - | getModels(): ?array | setModels(?array models): void |
| `method` | `?string` | Optional | Optional method identifier | getMethod(): ?string | setMethod(?string method): void |
| `tags` | `?(string[])` | Optional | Optional list of tags, null unless grouped by tags. | getTags(): ?array | setTags(?array tags): void |
| `deployment` | `?string` | Optional | Optional deployment identifier | getDeployment(): ?string | setDeployment(?string deployment): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\UsageBreakdownV1ResponseResultsItemsGroupingBuilder;
use DeepgramLib\Utils\DateTimeHelper;
use DeepgramLib\ApiHelper;

$usageBreakdownV1ResponseResultsItemsGrouping = UsageBreakdownV1ResponseResultsItemsGroupingBuilder::init()
    ->start(DateTimeHelper::fromSimpleDate('2016-03-13'))
    ->end(DateTimeHelper::fromSimpleDate('2016-03-13'))
    ->accessor('accessor8')
    ->endpoint('endpoint8')
    ->featureSet('feature_set0')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

