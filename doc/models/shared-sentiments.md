
# Shared Sentiments

Output whenever `sentiment=true` is used

*This model accepts additional fields of type array.*

## Structure

`SharedSentiments`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `segments` | [`?(SharedSentimentsSegmentsItems[])`](../../doc/models/shared-sentiments-segments-items.md) | Optional | - | getSegments(): ?array | setSegments(?array segments): void |
| `average` | [`?SharedSentimentsAverage`](../../doc/models/shared-sentiments-average.md) | Optional | - | getAverage(): ?SharedSentimentsAverage | setAverage(?SharedSentimentsAverage average): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\SharedSentimentsBuilder;
use DeepgramLib\Models\Builders\SharedSentimentsSegmentsItemsBuilder;
use DeepgramLib\ApiHelper;
use DeepgramLib\Models\Builders\SharedSentimentsAverageBuilder;

$sharedSentiments = SharedSentimentsBuilder::init()
    ->segments(
        [
            SharedSentimentsSegmentsItemsBuilder::init()
                ->text('text6')
                ->startWord(4.96)
                ->endWord(219.1)
                ->sentiment('sentiment6')
                ->sentimentScore(76.78)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
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
    ->build();
```

