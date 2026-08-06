
# Read V1 Response Results Summary Results Summary

*This model accepts additional fields of type array.*

## Structure

`ReadV1ResponseResultsSummaryResultsSummary`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `text` | `?string` | Optional | - | getText(): ?string | setText(?string text): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\ReadV1ResponseResultsSummaryResultsSummaryBuilder;
use DeepgramLib\ApiHelper;

$readV1ResponseResultsSummaryResultsSummary = ReadV1ResponseResultsSummaryResultsSummaryBuilder::init()
    ->text('text8')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

