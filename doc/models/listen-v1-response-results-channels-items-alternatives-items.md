
# Listen V1 Response Results Channels Items Alternatives Items

*This model accepts additional fields of type array.*

## Structure

`ListenV1ResponseResultsChannelsItemsAlternativesItems`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `transcript` | `?string` | Optional | - | getTranscript(): ?string | setTranscript(?string transcript): void |
| `confidence` | `?float` | Optional | - | getConfidence(): ?float | setConfidence(?float confidence): void |
| `words` | [`?(ListenV1ResponseResultsChannelsItemsAlternativesItemsWordsItems[])`](../../doc/models/listen-v1-response-results-channels-items-alternatives-items-words-items.md) | Optional | - | getWords(): ?array | setWords(?array words): void |
| `paragraphs` | [`?ListenV1ResponseResultsChannelsItemsAlternativesItemsParagraphs`](../../doc/models/listen-v1-response-results-channels-items-alternatives-items-paragraphs.md) | Optional | - | getParagraphs(): ?ListenV1ResponseResultsChannelsItemsAlternativesItemsParagraphs | setParagraphs(?ListenV1ResponseResultsChannelsItemsAlternativesItemsParagraphs paragraphs): void |
| `entities` | [`?(ListenV1ResponseResultsChannelsItemsAlternativesItemsEntitiesItems[])`](../../doc/models/listen-v1-response-results-channels-items-alternatives-items-entities-items.md) | Optional | - | getEntities(): ?array | setEntities(?array entities): void |
| `summaries` | [`?(ListenV1ResponseResultsChannelsItemsAlternativesItemsSummariesItems[])`](../../doc/models/listen-v1-response-results-channels-items-alternatives-items-summaries-items.md) | Optional | - | getSummaries(): ?array | setSummaries(?array summaries): void |
| `topics` | [`?(ListenV1ResponseResultsChannelsItemsAlternativesItemsTopicsItems[])`](../../doc/models/listen-v1-response-results-channels-items-alternatives-items-topics-items.md) | Optional | - | getTopics(): ?array | setTopics(?array topics): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\ListenV1ResponseResultsChannelsItemsAlternativesItemsBuilder;
use RestApiLib\Models\Builders\ListenV1ResponseResultsChannelsItemsAlternativesItemsWordsItemsBuilder;
use RestApiLib\ApiHelper;
use RestApiLib\Models\Builders\ListenV1ResponseResultsChannelsItemsAlternativesItemsParagraphsBuilder;
use RestApiLib\Models\Builders\ListenV1ResponseResultsChannelsItemsAlternativesItemsParagraphsParagraphsItemsBuilder;
use RestApiLib\Models\Builders\ListenV1ResponseResultsChannelsItemsAlternativesItemsParagraphsParagraphsItemsSentencesItemsBuilder;
use RestApiLib\Models\Builders\ListenV1ResponseResultsChannelsItemsAlternativesItemsEntitiesItemsBuilder;

$listenV1ResponseResultsChannelsItemsAlternativesItems = ListenV1ResponseResultsChannelsItemsAlternativesItemsBuilder::init()
    ->transcript('transcript6')
    ->confidence(101.86)
    ->words(
        [
            ListenV1ResponseResultsChannelsItemsAlternativesItemsWordsItemsBuilder::init()
                ->word('word0')
                ->start(58.62)
                ->end(102.56)
                ->confidence(56.72)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->paragraphs(
        ListenV1ResponseResultsChannelsItemsAlternativesItemsParagraphsBuilder::init()
            ->transcript('transcript2')
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
            ->build()
    )
    ->entities(
        [
            ListenV1ResponseResultsChannelsItemsAlternativesItemsEntitiesItemsBuilder::init()
                ->label('label0')
                ->value('value2')
                ->rawValue('raw_value6')
                ->confidence(136.04)
                ->startWord(101.8)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            ListenV1ResponseResultsChannelsItemsAlternativesItemsEntitiesItemsBuilder::init()
                ->label('label0')
                ->value('value2')
                ->rawValue('raw_value6')
                ->confidence(136.04)
                ->startWord(101.8)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

