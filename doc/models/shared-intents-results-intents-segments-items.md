
# Shared Intents Results Intents Segments Items

*This model accepts additional fields of type array.*

## Structure

`SharedIntentsResultsIntentsSegmentsItems`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `text` | `?string` | Optional | - | getText(): ?string | setText(?string text): void |
| `startWord` | `?float` | Optional | - | getStartWord(): ?float | setStartWord(?float startWord): void |
| `endWord` | `?float` | Optional | - | getEndWord(): ?float | setEndWord(?float endWord): void |
| `intents` | [`?(SharedIntentsResultsIntentsSegmentsItemsIntentsItems[])`](../../doc/models/shared-intents-results-intents-segments-items-intents-items.md) | Optional | - | getIntents(): ?array | setIntents(?array intents): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\SharedIntentsResultsIntentsSegmentsItemsBuilder;
use DeepgramLib\Models\Builders\SharedIntentsResultsIntentsSegmentsItemsIntentsItemsBuilder;
use DeepgramLib\ApiHelper;

$sharedIntentsResultsIntentsSegmentsItems = SharedIntentsResultsIntentsSegmentsItemsBuilder::init()
    ->text('text0')
    ->startWord(65.3)
    ->endWord(148.84)
    ->intents(
        [
            SharedIntentsResultsIntentsSegmentsItemsIntentsItemsBuilder::init()
                ->intent('intent4')
                ->confidenceScore(193.42)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            SharedIntentsResultsIntentsSegmentsItemsIntentsItemsBuilder::init()
                ->intent('intent4')
                ->confidenceScore(193.42)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            SharedIntentsResultsIntentsSegmentsItemsIntentsItemsBuilder::init()
                ->intent('intent4')
                ->confidenceScore(193.42)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

