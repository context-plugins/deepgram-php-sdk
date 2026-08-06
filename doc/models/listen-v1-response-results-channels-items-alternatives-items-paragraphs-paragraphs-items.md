
# Listen V1 Response Results Channels Items Alternatives Items Paragraphs Paragraphs Items

*This model accepts additional fields of type array.*

## Structure

`ListenV1ResponseResultsChannelsItemsAlternativesItemsParagraphsParagraphsItems`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `sentences` | [`?(ListenV1ResponseResultsChannelsItemsAlternativesItemsParagraphsParagraphsItemsSentencesItems[])`](../../doc/models/listen-v1-response-results-channels-items-alternatives-items-paragraphs-paragraphs-items-sentences-items.md) | Optional | - | getSentences(): ?array | setSentences(?array sentences): void |
| `speaker` | `?int` | Optional | - | getSpeaker(): ?int | setSpeaker(?int speaker): void |
| `numWords` | `?int` | Optional | - | getNumWords(): ?int | setNumWords(?int numWords): void |
| `start` | `?float` | Optional | - | getStart(): ?float | setStart(?float start): void |
| `end` | `?float` | Optional | - | getEnd(): ?float | setEnd(?float end): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\ListenV1ResponseResultsChannelsItemsAlternativesItemsParagraphsParagraphsItemsBuilder;
use DeepgramLib\Models\Builders\ListenV1ResponseResultsChannelsItemsAlternativesItemsParagraphsParagraphsItemsSentencesItemsBuilder;
use DeepgramLib\ApiHelper;

$listenV1ResponseResultsChannelsItemsAlternativesItemsParagraphsParagraphsItems = ListenV1ResponseResultsChannelsItemsAlternativesItemsParagraphsParagraphsItemsBuilder::init()
    ->sentences(
        [
            ListenV1ResponseResultsChannelsItemsAlternativesItemsParagraphsParagraphsItemsSentencesItemsBuilder::init()
                ->text('text2')
                ->start(16.92)
                ->end(60.86)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            ListenV1ResponseResultsChannelsItemsAlternativesItemsParagraphsParagraphsItemsSentencesItemsBuilder::init()
                ->text('text2')
                ->start(16.92)
                ->end(60.86)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            ListenV1ResponseResultsChannelsItemsAlternativesItemsParagraphsParagraphsItemsSentencesItemsBuilder::init()
                ->text('text2')
                ->start(16.92)
                ->end(60.86)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->speaker(32)
    ->numWords(220)
    ->start(74.44)
    ->end(118.38)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

