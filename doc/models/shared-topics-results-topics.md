
# Shared Topics Results Topics

*This model accepts additional fields of type array.*

## Structure

`SharedTopicsResultsTopics`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `segments` | [`?(SharedTopicsResultsTopicsSegmentsItems[])`](../../doc/models/shared-topics-results-topics-segments-items.md) | Optional | - | getSegments(): ?array | setSegments(?array segments): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\SharedTopicsResultsTopicsBuilder;
use DeepgramLib\Models\Builders\SharedTopicsResultsTopicsSegmentsItemsBuilder;
use DeepgramLib\Models\Builders\SharedTopicsResultsTopicsSegmentsItemsTopicsItemsBuilder;
use DeepgramLib\ApiHelper;

$sharedTopicsResultsTopics = SharedTopicsResultsTopicsBuilder::init()
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
    ->build();
```

