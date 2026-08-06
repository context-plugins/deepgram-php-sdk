
# Listen V1 Response Results Channels Items Alternatives Items Paragraphs

*This model accepts additional fields of type array.*

## Structure

`ListenV1ResponseResultsChannelsItemsAlternativesItemsParagraphs`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `transcript` | `?string` | Optional | - | getTranscript(): ?string | setTranscript(?string transcript): void |
| `paragraphs` | [`?(ListenV1ResponseResultsChannelsItemsAlternativesItemsParagraphsParagraphsItems[])`](../../doc/models/listen-v1-response-results-channels-items-alternatives-items-paragraphs-paragraphs-items.md) | Optional | - | getParagraphs(): ?array | setParagraphs(?array paragraphs): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\ListenV1ResponseResultsChannelsItemsAlternativesItemsParagraphsBuilder;
use DeepgramLib\Models\Builders\ListenV1ResponseResultsChannelsItemsAlternativesItemsParagraphsParagraphsItemsBuilder;
use DeepgramLib\Models\Builders\ListenV1ResponseResultsChannelsItemsAlternativesItemsParagraphsParagraphsItemsSentencesItemsBuilder;
use DeepgramLib\ApiHelper;

$listenV1ResponseResultsChannelsItemsAlternativesItemsParagraphs = ListenV1ResponseResultsChannelsItemsAlternativesItemsParagraphsBuilder::init()
    ->transcript('transcript4')
    ->paragraphs(
        [
            ListenV1ResponseResultsChannelsItemsAlternativesItemsParagraphsParagraphsItemsBuilder::init()
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
                            ->build()
                    ]
                )
                ->speaker(128)
                ->numWords(60)
                ->start(34.44)
                ->end(78.38)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            ListenV1ResponseResultsChannelsItemsAlternativesItemsParagraphsParagraphsItemsBuilder::init()
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
                            ->build()
                    ]
                )
                ->speaker(128)
                ->numWords(60)
                ->start(34.44)
                ->end(78.38)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

