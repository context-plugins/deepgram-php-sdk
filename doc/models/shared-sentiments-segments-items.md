
# Shared Sentiments Segments Items

*This model accepts additional fields of type array.*

## Structure

`SharedSentimentsSegmentsItems`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `text` | `?string` | Optional | - | getText(): ?string | setText(?string text): void |
| `startWord` | `?float` | Optional | - | getStartWord(): ?float | setStartWord(?float startWord): void |
| `endWord` | `?float` | Optional | - | getEndWord(): ?float | setEndWord(?float endWord): void |
| `sentiment` | `?string` | Optional | - | getSentiment(): ?string | setSentiment(?string sentiment): void |
| `sentimentScore` | `?float` | Optional | - | getSentimentScore(): ?float | setSentimentScore(?float sentimentScore): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\SharedSentimentsSegmentsItemsBuilder;
use RestApiLib\ApiHelper;

$sharedSentimentsSegmentsItems = SharedSentimentsSegmentsItemsBuilder::init()
    ->text('text2')
    ->startWord(75.32)
    ->endWord(138.82)
    ->sentiment('sentiment8')
    ->sentimentScore(252.5)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

