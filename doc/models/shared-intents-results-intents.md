
# Shared Intents Results Intents

*This model accepts additional fields of type array.*

## Structure

`SharedIntentsResultsIntents`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `segments` | [`?(SharedIntentsResultsIntentsSegmentsItems[])`](../../doc/models/shared-intents-results-intents-segments-items.md) | Optional | - | getSegments(): ?array | setSegments(?array segments): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\SharedIntentsResultsIntentsBuilder;
use DeepgramLib\Models\Builders\SharedIntentsResultsIntentsSegmentsItemsBuilder;
use DeepgramLib\Models\Builders\SharedIntentsResultsIntentsSegmentsItemsIntentsItemsBuilder;
use DeepgramLib\ApiHelper;

$sharedIntentsResultsIntents = SharedIntentsResultsIntentsBuilder::init()
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
                ->build(),
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
    ->build();
```

