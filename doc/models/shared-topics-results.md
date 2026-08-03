
# Shared Topics Results

*This model accepts additional fields of type array.*

## Structure

`SharedTopicsResults`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `topics` | [`?SharedTopicsResultsTopics`](../../doc/models/shared-topics-results-topics.md) | Optional | - | getTopics(): ?SharedTopicsResultsTopics | setTopics(?SharedTopicsResultsTopics topics): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\SharedTopicsResultsBuilder;
use RestApiLib\Models\Builders\SharedTopicsResultsTopicsBuilder;
use RestApiLib\Models\Builders\SharedTopicsResultsTopicsSegmentsItemsBuilder;
use RestApiLib\Models\Builders\SharedTopicsResultsTopicsSegmentsItemsTopicsItemsBuilder;
use RestApiLib\ApiHelper;

$sharedTopicsResults = SharedTopicsResultsBuilder::init()
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
    ->build();
```

