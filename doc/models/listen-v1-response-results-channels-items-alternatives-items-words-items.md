
# Listen V1 Response Results Channels Items Alternatives Items Words Items

*This model accepts additional fields of type array.*

## Structure

`ListenV1ResponseResultsChannelsItemsAlternativesItemsWordsItems`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `word` | `?string` | Optional | - | getWord(): ?string | setWord(?string word): void |
| `start` | `?float` | Optional | - | getStart(): ?float | setStart(?float start): void |
| `end` | `?float` | Optional | - | getEnd(): ?float | setEnd(?float end): void |
| `confidence` | `?float` | Optional | - | getConfidence(): ?float | setConfidence(?float confidence): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\ListenV1ResponseResultsChannelsItemsAlternativesItemsWordsItemsBuilder;
use RestApiLib\ApiHelper;

$listenV1ResponseResultsChannelsItemsAlternativesItemsWordsItems = ListenV1ResponseResultsChannelsItemsAlternativesItemsWordsItemsBuilder::init()
    ->word('word0')
    ->start(212.92)
    ->end(0.86)
    ->confidence(211.02)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

