
# Billing Breakdown V1 Response Results Items Grouping

*This model accepts additional fields of type array.*

## Structure

`BillingBreakdownV1ResponseResultsItemsGrouping`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `start` | `?DateTime` | Optional | Start date for this group | getStart(): ?\DateTime | setStart(?\DateTime start): void |
| `end` | `?DateTime` | Optional | End date for this group | getEnd(): ?\DateTime | setEnd(?\DateTime end): void |
| `accessor` | `?string` | Optional | Optional accessor identifier, null unless grouped by accessor. | getAccessor(): ?string | setAccessor(?string accessor): void |
| `deployment` | `?string` | Optional | Optional deployment identifier, null unless grouped by deployment. | getDeployment(): ?string | setDeployment(?string deployment): void |
| `lineItem` | `?string` | Optional | Optional line item identifier, null unless grouped by line item. | getLineItem(): ?string | setLineItem(?string lineItem): void |
| `tags` | `?(string[])` | Optional | Optional list of tags, null unless grouped by tags. | getTags(): ?array | setTags(?array tags): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\BillingBreakdownV1ResponseResultsItemsGroupingBuilder;
use DeepgramLib\Utils\DateTimeHelper;
use DeepgramLib\ApiHelper;

$billingBreakdownV1ResponseResultsItemsGrouping = BillingBreakdownV1ResponseResultsItemsGroupingBuilder::init()
    ->start(DateTimeHelper::fromSimpleDate('2016-03-13'))
    ->end(DateTimeHelper::fromSimpleDate('2016-03-13'))
    ->accessor('accessor8')
    ->deployment('deployment8')
    ->lineItem('line_item4')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

