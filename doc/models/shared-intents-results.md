
# Shared Intents Results

*This model accepts additional fields of type array.*

## Structure

`SharedIntentsResults`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `intents` | [`?SharedIntentsResultsIntents`](../../doc/models/shared-intents-results-intents.md) | Optional | - | getIntents(): ?SharedIntentsResultsIntents | setIntents(?SharedIntentsResultsIntents intents): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\SharedIntentsResultsBuilder;
use RestApiLib\Models\Builders\SharedIntentsResultsIntentsBuilder;
use RestApiLib\Models\Builders\SharedIntentsResultsIntentsSegmentsItemsBuilder;
use RestApiLib\Models\Builders\SharedIntentsResultsIntentsSegmentsItemsIntentsItemsBuilder;
use RestApiLib\ApiHelper;

$sharedIntentsResults = SharedIntentsResultsBuilder::init()
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
    ->build();
```

