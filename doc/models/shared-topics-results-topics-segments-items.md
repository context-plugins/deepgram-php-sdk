
# Shared Topics Results Topics Segments Items

*This model accepts additional fields of type array.*

## Structure

`SharedTopicsResultsTopicsSegmentsItems`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `text` | `?string` | Optional | - | getText(): ?string | setText(?string text): void |
| `startWord` | `?float` | Optional | - | getStartWord(): ?float | setStartWord(?float startWord): void |
| `endWord` | `?float` | Optional | - | getEndWord(): ?float | setEndWord(?float endWord): void |
| `topics` | [`?(SharedTopicsResultsTopicsSegmentsItemsTopicsItems[])`](../../doc/models/shared-topics-results-topics-segments-items-topics-items.md) | Optional | - | getTopics(): ?array | setTopics(?array topics): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\SharedTopicsResultsTopicsSegmentsItemsBuilder;
use RestApiLib\Models\Builders\SharedTopicsResultsTopicsSegmentsItemsTopicsItemsBuilder;
use RestApiLib\ApiHelper;

$sharedTopicsResultsTopicsSegmentsItems = SharedTopicsResultsTopicsSegmentsItemsBuilder::init()
    ->text('text0')
    ->startWord(138.4)
    ->endWord(96.54)
    ->topics(
        [
            SharedTopicsResultsTopicsSegmentsItemsTopicsItemsBuilder::init()
                ->topic('topic2')
                ->confidenceScore(42.46)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

