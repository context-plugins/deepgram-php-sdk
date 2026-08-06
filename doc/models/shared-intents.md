
# Shared Intents

Output whenever `intents=true` is used

*This model accepts additional fields of type array.*

## Structure

`SharedIntents`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `results` | [`?SharedIntentsResults`](../../doc/models/shared-intents-results.md) | Optional | - | getResults(): ?SharedIntentsResults | setResults(?SharedIntentsResults results): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\SharedIntentsBuilder;
use DeepgramLib\Models\Builders\SharedIntentsResultsBuilder;
use DeepgramLib\Models\Builders\SharedIntentsResultsIntentsBuilder;
use DeepgramLib\Models\Builders\SharedIntentsResultsIntentsSegmentsItemsBuilder;
use DeepgramLib\Models\Builders\SharedIntentsResultsIntentsSegmentsItemsIntentsItemsBuilder;
use DeepgramLib\ApiHelper;

$sharedIntents = SharedIntentsBuilder::init()
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
    ->build();
```

