
# Usage V1 Response

*This model accepts additional fields of type array.*

## Structure

`UsageV1Response`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `start` | `?DateTime` | Optional | - | getStart(): ?\DateTime | setStart(?\DateTime start): void |
| `end` | `?DateTime` | Optional | - | getEnd(): ?\DateTime | setEnd(?\DateTime end): void |
| `resolution` | [`?UsageV1ResponseResolution`](../../doc/models/usage-v1-response-resolution.md) | Optional | - | getResolution(): ?UsageV1ResponseResolution | setResolution(?UsageV1ResponseResolution resolution): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\UsageV1ResponseBuilder;
use DeepgramLib\Utils\DateTimeHelper;
use DeepgramLib\Models\Builders\UsageV1ResponseResolutionBuilder;
use DeepgramLib\ApiHelper;

$usageV1Response = UsageV1ResponseBuilder::init()
    ->start(DateTimeHelper::fromSimpleDate('2016-03-13'))
    ->end(DateTimeHelper::fromSimpleDate('2016-03-13'))
    ->resolution(
        UsageV1ResponseResolutionBuilder::init()
            ->units('units8')
            ->amount(98.28)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

