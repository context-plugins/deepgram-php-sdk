
# Listen V1 Response Results Channels Items Search Items Hits Items

*This model accepts additional fields of type array.*

## Structure

`ListenV1ResponseResultsChannelsItemsSearchItemsHitsItems`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `confidence` | `?float` | Optional | - | getConfidence(): ?float | setConfidence(?float confidence): void |
| `start` | `?float` | Optional | - | getStart(): ?float | setStart(?float start): void |
| `end` | `?float` | Optional | - | getEnd(): ?float | setEnd(?float end): void |
| `snippet` | `?string` | Optional | - | getSnippet(): ?string | setSnippet(?string snippet): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\ListenV1ResponseResultsChannelsItemsSearchItemsHitsItemsBuilder;
use DeepgramLib\ApiHelper;

$listenV1ResponseResultsChannelsItemsSearchItemsHitsItems = ListenV1ResponseResultsChannelsItemsSearchItemsHitsItemsBuilder::init()
    ->confidence(94.16)
    ->start(96.06)
    ->end(140)
    ->snippet('snippet8')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

