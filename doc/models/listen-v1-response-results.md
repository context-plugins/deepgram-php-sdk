
# Listen V1 Response Results

*This model accepts additional fields of type array.*

## Structure

`ListenV1ResponseResults`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `channels` | [`ListenV1ResponseResultsChannelsItems[]`](../../doc/models/listen-v1-response-results-channels-items.md) | Required | - | getChannels(): array | setChannels(array channels): void |
| `utterances` | [`?(ListenV1ResponseResultsUtterancesItems[])`](../../doc/models/listen-v1-response-results-utterances-items.md) | Optional | - | getUtterances(): ?array | setUtterances(?array utterances): void |
| `summary` | [`?ListenV1ResponseResultsSummary`](../../doc/models/listen-v1-response-results-summary.md) | Optional | - | getSummary(): ?ListenV1ResponseResultsSummary | setSummary(?ListenV1ResponseResultsSummary summary): void |
| `topics` | [`?SharedTopics`](../../doc/models/shared-topics.md) | Optional | Output whenever `topics=true` is used | getTopics(): ?SharedTopics | setTopics(?SharedTopics topics): void |
| `intents` | [`?SharedIntents`](../../doc/models/shared-intents.md) | Optional | Output whenever `intents=true` is used | getIntents(): ?SharedIntents | setIntents(?SharedIntents intents): void |
| `sentiments` | [`?SharedSentiments`](../../doc/models/shared-sentiments.md) | Optional | Output whenever `sentiment=true` is used | getSentiments(): ?SharedSentiments | setSentiments(?SharedSentiments sentiments): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\ListenV1ResponseResultsBuilder;
use RestApiLib\Models\Builders\ListenV1ResponseResultsChannelsItemsBuilder;
use RestApiLib\Models\Builders\ListenV1ResponseResultsChannelsItemsSearchItemsBuilder;
use RestApiLib\Models\Builders\ListenV1ResponseResultsChannelsItemsSearchItemsHitsItemsBuilder;
use RestApiLib\ApiHelper;
use RestApiLib\Models\Builders\ListenV1ResponseResultsChannelsItemsAlternativesItemsBuilder;
use RestApiLib\Models\Builders\ListenV1ResponseResultsChannelsItemsAlternativesItemsWordsItemsBuilder;
use RestApiLib\Models\Builders\ListenV1ResponseResultsChannelsItemsAlternativesItemsParagraphsBuilder;
use RestApiLib\Models\Builders\ListenV1ResponseResultsChannelsItemsAlternativesItemsParagraphsParagraphsItemsBuilder;
use RestApiLib\Models\Builders\ListenV1ResponseResultsChannelsItemsAlternativesItemsParagraphsParagraphsItemsSentencesItemsBuilder;
use RestApiLib\Models\Builders\ListenV1ResponseResultsChannelsItemsAlternativesItemsEntitiesItemsBuilder;
use RestApiLib\Models\Builders\ListenV1ResponseResultsUtterancesItemsBuilder;
use RestApiLib\Models\Builders\ListenV1ResponseResultsSummaryBuilder;
use RestApiLib\Models\Builders\SharedTopicsBuilder;
use RestApiLib\Models\Builders\SharedTopicsResultsBuilder;
use RestApiLib\Models\Builders\SharedTopicsResultsTopicsBuilder;
use RestApiLib\Models\Builders\SharedTopicsResultsTopicsSegmentsItemsBuilder;
use RestApiLib\Models\Builders\SharedTopicsResultsTopicsSegmentsItemsTopicsItemsBuilder;
use RestApiLib\Models\Builders\SharedIntentsBuilder;
use RestApiLib\Models\Builders\SharedIntentsResultsBuilder;
use RestApiLib\Models\Builders\SharedIntentsResultsIntentsBuilder;
use RestApiLib\Models\Builders\SharedIntentsResultsIntentsSegmentsItemsBuilder;
use RestApiLib\Models\Builders\SharedIntentsResultsIntentsSegmentsItemsIntentsItemsBuilder;
use RestApiLib\Models\Builders\SharedSentimentsBuilder;
use RestApiLib\Models\Builders\SharedSentimentsSegmentsItemsBuilder;
use RestApiLib\Models\Builders\SharedSentimentsAverageBuilder;

$listenV1ResponseResults = ListenV1ResponseResultsBuilder::init(
    [
        ListenV1ResponseResultsChannelsItemsBuilder::init()
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
                        ->build(),
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
                        ->build(),
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
            ->detectedLanguage('detected_language0')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    ]
)
    ->utterances(
        [
            ListenV1ResponseResultsUtterancesItemsBuilder::init()
                ->start(249.82)
                ->end(37.76)
                ->confidence(247.92)
                ->channel(182)
                ->transcript('transcript0')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->summary(
        ListenV1ResponseResultsSummaryBuilder::init()
            ->result('result4')
            ->short('short8')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->topics(
        SharedTopicsBuilder::init()
            ->results(
                SharedTopicsResultsBuilder::init()
                    ->topics(
                        SharedTopicsResultsTopicsBuilder::init()
                            ->segments(
                                [
                                    SharedTopicsResultsTopicsSegmentsItemsBuilder::init()
                                        ->text('text6')
                                        ->startWord(4.96)
                                        ->endWord(219.1)
                                        ->topics(
                                            [
                                                SharedTopicsResultsTopicsSegmentsItemsTopicsItemsBuilder::init()
                                                    ->topic('topic2')
                                                    ->confidenceScore(42.46)
                                                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                                    ->build(),
                                                SharedTopicsResultsTopicsSegmentsItemsTopicsItemsBuilder::init()
                                                    ->topic('topic2')
                                                    ->confidenceScore(42.46)
                                                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                                    ->build()
                                            ]
                                        )
                                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                        ->build()
                                ]
                            )
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build()
                    )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->intents(
        SharedIntentsBuilder::init()
            ->results(
                SharedIntentsResultsBuilder::init()
                    ->intents(
                        SharedIntentsResultsIntentsBuilder::init()
                            ->segments(
                                [
                                    SharedIntentsResultsIntentsSegmentsItemsBuilder::init()
                                        ->text('text6')
                                        ->startWord(4.96)
                                        ->endWord(219.1)
                                        ->intents(
                                            [
                                                SharedIntentsResultsIntentsSegmentsItemsIntentsItemsBuilder::init()
                                                    ->intent('intent4')
                                                    ->confidenceScore(193.42)
                                                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                                    ->build()
                                            ]
                                        )
                                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                        ->build()
                                ]
                            )
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build()
                    )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->sentiments(
        SharedSentimentsBuilder::init()
            ->segments(
                [
                    SharedSentimentsSegmentsItemsBuilder::init()
                        ->text('text6')
                        ->startWord(4.96)
                        ->endWord(219.1)
                        ->sentiment('sentiment6')
                        ->sentimentScore(76.78)
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                ]
            )
            ->average(
                SharedSentimentsAverageBuilder::init()
                    ->sentiment('sentiment8')
                    ->sentimentScore(2.7)
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

