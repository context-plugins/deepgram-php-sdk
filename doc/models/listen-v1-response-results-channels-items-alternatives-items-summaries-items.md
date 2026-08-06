
# Listen V1 Response Results Channels Items Alternatives Items Summaries Items

*This model accepts additional fields of type array.*

## Structure

`ListenV1ResponseResultsChannelsItemsAlternativesItemsSummariesItems`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `summary` | `?string` | Optional | - | getSummary(): ?string | setSummary(?string summary): void |
| `startWord` | `?float` | Optional | - | getStartWord(): ?float | setStartWord(?float startWord): void |
| `endWord` | `?float` | Optional | - | getEndWord(): ?float | setEndWord(?float endWord): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\ListenV1ResponseResultsChannelsItemsAlternativesItemsSummariesItemsBuilder;
use DeepgramLib\ApiHelper;

$listenV1ResponseResultsChannelsItemsAlternativesItemsSummariesItems = ListenV1ResponseResultsChannelsItemsAlternativesItemsSummariesItemsBuilder::init()
    ->summary('summary8')
    ->startWord(11.54)
    ->endWord(53.4)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

