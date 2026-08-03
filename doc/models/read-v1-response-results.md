
# Read V1 Response Results

*This model accepts additional fields of type array.*

## Structure

`ReadV1ResponseResults`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `summary` | [`?ReadV1ResponseResultsSummary`](../../doc/models/read-v1-response-results-summary.md) | Optional | Output whenever `summary=true` is used | getSummary(): ?ReadV1ResponseResultsSummary | setSummary(?ReadV1ResponseResultsSummary summary): void |
| `topics` | [`?SharedTopics`](../../doc/models/shared-topics.md) | Optional | Output whenever `topics=true` is used | getTopics(): ?SharedTopics | setTopics(?SharedTopics topics): void |
| `intents` | [`?SharedIntents`](../../doc/models/shared-intents.md) | Optional | Output whenever `intents=true` is used | getIntents(): ?SharedIntents | setIntents(?SharedIntents intents): void |
| `sentiments` | [`?SharedSentiments`](../../doc/models/shared-sentiments.md) | Optional | Output whenever `sentiment=true` is used | getSentiments(): ?SharedSentiments | setSentiments(?SharedSentiments sentiments): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\ReadV1ResponseResultsBuilder;
use RestApiLib\Models\Builders\ReadV1ResponseResultsSummaryBuilder;
use RestApiLib\Models\Builders\ReadV1ResponseResultsSummaryResultsBuilder;
use RestApiLib\Models\Builders\ReadV1ResponseResultsSummaryResultsSummaryBuilder;
use RestApiLib\ApiHelper;
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

$readV1ResponseResults = ReadV1ResponseResultsBuilder::init()
    ->summary(
        ReadV1ResponseResultsSummaryBuilder::init()
            ->results(
                ReadV1ResponseResultsSummaryResultsBuilder::init()
                    ->summary(
                        ReadV1ResponseResultsSummaryResultsSummaryBuilder::init()
                            ->text('text8')
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build()
                    )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
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

