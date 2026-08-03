
# Shared Topics Results Topics Segments Items Topics Items

*This model accepts additional fields of type array.*

## Structure

`SharedTopicsResultsTopicsSegmentsItemsTopicsItems`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `topic` | `?string` | Optional | - | getTopic(): ?string | setTopic(?string topic): void |
| `confidenceScore` | `?float` | Optional | - | getConfidenceScore(): ?float | setConfidenceScore(?float confidenceScore): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\SharedTopicsResultsTopicsSegmentsItemsTopicsItemsBuilder;
use RestApiLib\ApiHelper;

$sharedTopicsResultsTopicsSegmentsItemsTopicsItems = SharedTopicsResultsTopicsSegmentsItemsTopicsItemsBuilder::init()
    ->topic('topic8')
    ->confidenceScore(62.12)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

