
# Shared Intents Results Intents Segments Items Intents Items

*This model accepts additional fields of type array.*

## Structure

`SharedIntentsResultsIntentsSegmentsItemsIntentsItems`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `intent` | `?string` | Optional | - | getIntent(): ?string | setIntent(?string intent): void |
| `confidenceScore` | `?float` | Optional | - | getConfidenceScore(): ?float | setConfidenceScore(?float confidenceScore): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\SharedIntentsResultsIntentsSegmentsItemsIntentsItemsBuilder;
use RestApiLib\ApiHelper;

$sharedIntentsResultsIntentsSegmentsItemsIntentsItems = SharedIntentsResultsIntentsSegmentsItemsIntentsItemsBuilder::init()
    ->intent('intent6')
    ->confidenceScore(63.1)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

