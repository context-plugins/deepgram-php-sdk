
# Shared Topics

Output whenever `topics=true` is used

*This model accepts additional fields of type array.*

## Structure

`SharedTopics`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `results` | [`?SharedTopicsResults`](../../doc/models/shared-topics-results.md) | Optional | - | getResults(): ?SharedTopicsResults | setResults(?SharedTopicsResults results): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\SharedTopicsBuilder;
use RestApiLib\Models\Builders\SharedTopicsResultsBuilder;
use RestApiLib\Models\Builders\SharedTopicsResultsTopicsBuilder;
use RestApiLib\Models\Builders\SharedTopicsResultsTopicsSegmentsItemsBuilder;
use RestApiLib\Models\Builders\SharedTopicsResultsTopicsSegmentsItemsTopicsItemsBuilder;
use RestApiLib\ApiHelper;

$sharedTopics = SharedTopicsBuilder::init()
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
    ->build();
```

