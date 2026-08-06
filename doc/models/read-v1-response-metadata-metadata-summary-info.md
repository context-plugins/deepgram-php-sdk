
# Read V1 Response Metadata Metadata Summary Info

*This model accepts additional fields of type array.*

## Structure

`ReadV1ResponseMetadataMetadataSummaryInfo`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `modelUuid` | `?string` | Optional | - | getModelUuid(): ?string | setModelUuid(?string modelUuid): void |
| `inputTokens` | `?int` | Optional | - | getInputTokens(): ?int | setInputTokens(?int inputTokens): void |
| `outputTokens` | `?int` | Optional | - | getOutputTokens(): ?int | setOutputTokens(?int outputTokens): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\ReadV1ResponseMetadataMetadataSummaryInfoBuilder;
use DeepgramLib\ApiHelper;

$readV1ResponseMetadataMetadataSummaryInfo = ReadV1ResponseMetadataMetadataSummaryInfoBuilder::init()
    ->modelUuid('0000078a-0000-0000-0000-000000000000')
    ->inputTokens(128)
    ->outputTokens(128)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

