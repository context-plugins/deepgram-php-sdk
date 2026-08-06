
# Listen V1 Response Results Channels Items Alternatives Items Topics Items

*This model accepts additional fields of type array.*

## Structure

`ListenV1ResponseResultsChannelsItemsAlternativesItemsTopicsItems`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `text` | `?string` | Optional | - | getText(): ?string | setText(?string text): void |
| `startWord` | `?float` | Optional | - | getStartWord(): ?float | setStartWord(?float startWord): void |
| `endWord` | `?float` | Optional | - | getEndWord(): ?float | setEndWord(?float endWord): void |
| `topics` | `?(string[])` | Optional | - | getTopics(): ?array | setTopics(?array topics): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\ListenV1ResponseResultsChannelsItemsAlternativesItemsTopicsItemsBuilder;
use DeepgramLib\ApiHelper;

$listenV1ResponseResultsChannelsItemsAlternativesItemsTopicsItems = ListenV1ResponseResultsChannelsItemsAlternativesItemsTopicsItemsBuilder::init()
    ->text('text2')
    ->startWord(38.88)
    ->endWord(253.02)
    ->topics(
        [
            'topics7',
            'topics8',
            'topics9'
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

