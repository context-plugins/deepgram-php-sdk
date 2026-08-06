
# Read V1 Response Results Summary

Output whenever `summary=true` is used

*This model accepts additional fields of type array.*

## Structure

`ReadV1ResponseResultsSummary`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `results` | [`?ReadV1ResponseResultsSummaryResults`](../../doc/models/read-v1-response-results-summary-results.md) | Optional | - | getResults(): ?ReadV1ResponseResultsSummaryResults | setResults(?ReadV1ResponseResultsSummaryResults results): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\ReadV1ResponseResultsSummaryBuilder;
use DeepgramLib\Models\Builders\ReadV1ResponseResultsSummaryResultsBuilder;
use DeepgramLib\Models\Builders\ReadV1ResponseResultsSummaryResultsSummaryBuilder;
use DeepgramLib\ApiHelper;

$readV1ResponseResultsSummary = ReadV1ResponseResultsSummaryBuilder::init()
    ->results(
        ReadV1ResponseResultsSummaryResultsBuilder::init()
            ->summary(
                ReadV1ResponseResultsSummaryResultsSummaryBuilder::init()
                    ->text('text8')
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

