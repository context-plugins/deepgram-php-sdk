
# Shared Sentiments Average

*This model accepts additional fields of type array.*

## Structure

`SharedSentimentsAverage`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `sentiment` | `?string` | Optional | - | getSentiment(): ?string | setSentiment(?string sentiment): void |
| `sentimentScore` | `?float` | Optional | - | getSentimentScore(): ?float | setSentimentScore(?float sentimentScore): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\SharedSentimentsAverageBuilder;
use DeepgramLib\ApiHelper;

$sharedSentimentsAverage = SharedSentimentsAverageBuilder::init()
    ->sentiment('sentiment2')
    ->sentimentScore(148.84)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

