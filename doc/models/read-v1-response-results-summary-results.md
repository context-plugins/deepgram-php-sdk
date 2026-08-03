
# Read V1 Response Results Summary Results

*This model accepts additional fields of type array.*

## Structure

`ReadV1ResponseResultsSummaryResults`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `summary` | [`?ReadV1ResponseResultsSummaryResultsSummary`](../../doc/models/read-v1-response-results-summary-results-summary.md) | Optional | - | getSummary(): ?ReadV1ResponseResultsSummaryResultsSummary | setSummary(?ReadV1ResponseResultsSummaryResultsSummary summary): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\ReadV1ResponseResultsSummaryResultsBuilder;
use RestApiLib\Models\Builders\ReadV1ResponseResultsSummaryResultsSummaryBuilder;
use RestApiLib\ApiHelper;

$readV1ResponseResultsSummaryResults = ReadV1ResponseResultsSummaryResultsBuilder::init()
    ->summary(
        ReadV1ResponseResultsSummaryResultsSummaryBuilder::init()
            ->text('text8')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

