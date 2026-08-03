
# Listen V1 Response Results Channels Items Alternatives Items Paragraphs Paragraphs Items Sentences Items

*This model accepts additional fields of type array.*

## Structure

`ListenV1ResponseResultsChannelsItemsAlternativesItemsParagraphsParagraphsItemsSentencesItems`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `text` | `?string` | Optional | - | getText(): ?string | setText(?string text): void |
| `start` | `?float` | Optional | - | getStart(): ?float | setStart(?float start): void |
| `end` | `?float` | Optional | - | getEnd(): ?float | setEnd(?float end): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\ListenV1ResponseResultsChannelsItemsAlternativesItemsParagraphsParagraphsItemsSentencesItemsBuilder;
use RestApiLib\ApiHelper;

$listenV1ResponseResultsChannelsItemsAlternativesItemsParagraphsParagraphsItemsSentencesItems = ListenV1ResponseResultsChannelsItemsAlternativesItemsParagraphsParagraphsItemsSentencesItemsBuilder::init()
    ->text('text6')
    ->start(243.88)
    ->end(31.82)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

