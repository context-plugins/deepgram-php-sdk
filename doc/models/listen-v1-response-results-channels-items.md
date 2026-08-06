
# Listen V1 Response Results Channels Items

*This model accepts additional fields of type array.*

## Structure

`ListenV1ResponseResultsChannelsItems`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `search` | [`?(ListenV1ResponseResultsChannelsItemsSearchItems[])`](../../doc/models/listen-v1-response-results-channels-items-search-items.md) | Optional | - | getSearch(): ?array | setSearch(?array search): void |
| `alternatives` | [`?(ListenV1ResponseResultsChannelsItemsAlternativesItems[])`](../../doc/models/listen-v1-response-results-channels-items-alternatives-items.md) | Optional | - | getAlternatives(): ?array | setAlternatives(?array alternatives): void |
| `detectedLanguage` | `?string` | Optional | - | getDetectedLanguage(): ?string | setDetectedLanguage(?string detectedLanguage): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\ListenV1ResponseResultsChannelsItemsBuilder;
use DeepgramLib\Models\Builders\ListenV1ResponseResultsChannelsItemsSearchItemsBuilder;
use DeepgramLib\Models\Builders\ListenV1ResponseResultsChannelsItemsSearchItemsHitsItemsBuilder;
use DeepgramLib\ApiHelper;
use DeepgramLib\Models\Builders\ListenV1ResponseResultsChannelsItemsAlternativesItemsBuilder;
use DeepgramLib\Models\Builders\ListenV1ResponseResultsChannelsItemsAlternativesItemsWordsItemsBuilder;
use DeepgramLib\Models\Builders\ListenV1ResponseResultsChannelsItemsAlternativesItemsParagraphsBuilder;
use DeepgramLib\Models\Builders\ListenV1ResponseResultsChannelsItemsAlternativesItemsParagraphsParagraphsItemsBuilder;
use DeepgramLib\Models\Builders\ListenV1ResponseResultsChannelsItemsAlternativesItemsParagraphsParagraphsItemsSentencesItemsBuilder;
use DeepgramLib\Models\Builders\ListenV1ResponseResultsChannelsItemsAlternativesItemsEntitiesItemsBuilder;

$listenV1ResponseResultsChannelsItems = ListenV1ResponseResultsChannelsItemsBuilder::init()
    ->search(
        [
            ListenV1ResponseResultsChannelsItemsSearchItemsBuilder::init()
                ->query('query2')
                ->hits(
                    [
                        ListenV1ResponseResultsChannelsItemsSearchItemsHitsItemsBuilder::init()
                            ->confidence(144.74)
                            ->start(146.64)
                            ->end(190.58)
                            ->snippet('snippet0')
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build()
                    ]
                )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->alternatives(
        [
            ListenV1ResponseResultsChannelsItemsAlternativesItemsBuilder::init()
                ->transcript('transcript6')
                ->confidence(34.78)
                ->words(
                    [
                        ListenV1ResponseResultsChannelsItemsAlternativesItemsWordsItemsBuilder::init()
                            ->word('word0')
                            ->start(58.62)
                            ->end(102.56)
                            ->confidence(56.72)
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build(),
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
                ->build()
        ]
    )
    ->detectedLanguage('detected_language4')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

