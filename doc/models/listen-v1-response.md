
# Listen V1 Response

The standard transcription response

*This model accepts additional fields of type array.*

## Structure

`ListenV1Response`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `metadata` | [`ListenV1ResponseMetadata`](../../doc/models/listen-v1-response-metadata.md) | Required | - | getMetadata(): ListenV1ResponseMetadata | setMetadata(ListenV1ResponseMetadata metadata): void |
| `results` | [`ListenV1ResponseResults`](../../doc/models/listen-v1-response-results.md) | Required | - | getResults(): ListenV1ResponseResults | setResults(ListenV1ResponseResults results): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\ListenV1ResponseBuilder;
use DeepgramLib\Models\Builders\ListenV1ResponseMetadataBuilder;
use DeepgramLib\Utils\DateTimeHelper;
use DeepgramLib\ApiHelper;
use DeepgramLib\Models\Builders\ListenV1ResponseMetadataSummaryInfoBuilder;
use DeepgramLib\Models\Builders\ListenV1ResponseMetadataSentimentInfoBuilder;
use DeepgramLib\Models\Builders\ListenV1ResponseMetadataTopicsInfoBuilder;
use DeepgramLib\Models\Builders\ListenV1ResponseMetadataIntentsInfoBuilder;
use DeepgramLib\Models\Builders\ListenV1ResponseResultsBuilder;
use DeepgramLib\Models\Builders\ListenV1ResponseResultsChannelsItemsBuilder;
use DeepgramLib\Models\Builders\ListenV1ResponseResultsChannelsItemsSearchItemsBuilder;
use DeepgramLib\Models\Builders\ListenV1ResponseResultsChannelsItemsSearchItemsHitsItemsBuilder;
use DeepgramLib\Models\Builders\ListenV1ResponseResultsChannelsItemsAlternativesItemsBuilder;
use DeepgramLib\Models\Builders\ListenV1ResponseResultsChannelsItemsAlternativesItemsWordsItemsBuilder;
use DeepgramLib\Models\Builders\ListenV1ResponseResultsChannelsItemsAlternativesItemsParagraphsBuilder;
use DeepgramLib\Models\Builders\ListenV1ResponseResultsChannelsItemsAlternativesItemsParagraphsParagraphsItemsBuilder;
use DeepgramLib\Models\Builders\ListenV1ResponseResultsChannelsItemsAlternativesItemsParagraphsParagraphsItemsSentencesItemsBuilder;
use DeepgramLib\Models\Builders\ListenV1ResponseResultsChannelsItemsAlternativesItemsEntitiesItemsBuilder;
use DeepgramLib\Models\Builders\ListenV1ResponseResultsUtterancesItemsBuilder;
use DeepgramLib\Models\Builders\ListenV1ResponseResultsSummaryBuilder;
use DeepgramLib\Models\Builders\SharedTopicsBuilder;
use DeepgramLib\Models\Builders\SharedTopicsResultsBuilder;
use DeepgramLib\Models\Builders\SharedTopicsResultsTopicsBuilder;
use DeepgramLib\Models\Builders\SharedTopicsResultsTopicsSegmentsItemsBuilder;
use DeepgramLib\Models\Builders\SharedTopicsResultsTopicsSegmentsItemsTopicsItemsBuilder;
use DeepgramLib\Models\Builders\SharedIntentsBuilder;
use DeepgramLib\Models\Builders\SharedIntentsResultsBuilder;
use DeepgramLib\Models\Builders\SharedIntentsResultsIntentsBuilder;
use DeepgramLib\Models\Builders\SharedIntentsResultsIntentsSegmentsItemsBuilder;
use DeepgramLib\Models\Builders\SharedIntentsResultsIntentsSegmentsItemsIntentsItemsBuilder;
use DeepgramLib\Models\Builders\SharedSentimentsBuilder;
use DeepgramLib\Models\Builders\SharedSentimentsSegmentsItemsBuilder;
use DeepgramLib\Models\Builders\SharedSentimentsAverageBuilder;

$listenV1Response = ListenV1ResponseBuilder::init(
    ListenV1ResponseMetadataBuilder::init(
        '000018ae-0000-0000-0000-000000000000',
        'sha2568',
        DateTimeHelper::fromRfc3339DateTimeRequired('2016-03-13T12:52:32.123Z'),
        108.02,
        44,
        [
            'models2'
        ],
        ApiHelper::deserialize('{"key1":"val1","key2":"val2"}')
    )
        ->transactionKey('deprecated')
        ->summaryInfo(
            ListenV1ResponseMetadataSummaryInfoBuilder::init()
                ->modelUuid('model_uuid4')
                ->inputTokens(120)
                ->outputTokens(120)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        )
        ->sentimentInfo(
            ListenV1ResponseMetadataSentimentInfoBuilder::init()
                ->modelUuid('model_uuid6')
                ->inputTokens(86)
                ->outputTokens(86)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        )
        ->topicsInfo(
            ListenV1ResponseMetadataTopicsInfoBuilder::init()
                ->modelUuid('model_uuid8')
                ->inputTokens(156)
                ->outputTokens(156)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        )
        ->intentsInfo(
            ListenV1ResponseMetadataIntentsInfoBuilder::init()
                ->modelUuid('model_uuid6')
                ->inputTokens(198)
                ->outputTokens(198)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build(),
    ListenV1ResponseResultsBuilder::init(
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
                    ->build(),
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
        ->build()
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

