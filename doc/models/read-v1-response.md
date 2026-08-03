
# Read V1 Response

The standard text response

*This model accepts additional fields of type array.*

## Structure

`ReadV1Response`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `metadata` | [`ReadV1ResponseMetadata`](../../doc/models/read-v1-response-metadata.md) | Required | - | getMetadata(): ReadV1ResponseMetadata | setMetadata(ReadV1ResponseMetadata metadata): void |
| `results` | [`ReadV1ResponseResults`](../../doc/models/read-v1-response-results.md) | Required | - | getResults(): ReadV1ResponseResults | setResults(ReadV1ResponseResults results): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\ReadV1ResponseBuilder;
use RestApiLib\Models\Builders\ReadV1ResponseMetadataBuilder;
use RestApiLib\Models\Builders\ReadV1ResponseMetadataMetadataBuilder;
use RestApiLib\Utils\DateTimeHelper;
use RestApiLib\Models\Builders\ReadV1ResponseMetadataMetadataSummaryInfoBuilder;
use RestApiLib\ApiHelper;
use RestApiLib\Models\Builders\ReadV1ResponseMetadataMetadataSentimentInfoBuilder;
use RestApiLib\Models\Builders\ReadV1ResponseResultsBuilder;
use RestApiLib\Models\Builders\ReadV1ResponseResultsSummaryBuilder;
use RestApiLib\Models\Builders\ReadV1ResponseResultsSummaryResultsBuilder;
use RestApiLib\Models\Builders\ReadV1ResponseResultsSummaryResultsSummaryBuilder;
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

$readV1Response = ReadV1ResponseBuilder::init(
    ReadV1ResponseMetadataBuilder::init()
        ->metadata(
            ReadV1ResponseMetadataMetadataBuilder::init()
                ->requestId('000018ae-0000-0000-0000-000000000000')
                ->created(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                ->language('language8')
                ->summaryInfo(
                    ReadV1ResponseMetadataMetadataSummaryInfoBuilder::init()
                        ->modelUuid('00000e32-0000-0000-0000-000000000000')
                        ->inputTokens(120)
                        ->outputTokens(120)
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->sentimentInfo(
                    ReadV1ResponseMetadataMetadataSentimentInfoBuilder::init()
                        ->modelUuid('00001640-0000-0000-0000-000000000000')
                        ->inputTokens(86)
                        ->outputTokens(86)
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build(),
    ReadV1ResponseResultsBuilder::init()
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
        ->build()
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

