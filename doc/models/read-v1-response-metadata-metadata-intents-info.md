
# Read V1 Response Metadata Metadata Intents Info

*This model accepts additional fields of type array.*

## Structure

`ReadV1ResponseMetadataMetadataIntentsInfo`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `modelUuid` | `?string` | Optional | - | getModelUuid(): ?string | setModelUuid(?string modelUuid): void |
| `inputTokens` | `?int` | Optional | - | getInputTokens(): ?int | setInputTokens(?int inputTokens): void |
| `outputTokens` | `?int` | Optional | - | getOutputTokens(): ?int | setOutputTokens(?int outputTokens): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\ReadV1ResponseMetadataMetadataIntentsInfoBuilder;
use RestApiLib\ApiHelper;

$readV1ResponseMetadataMetadataIntentsInfo = ReadV1ResponseMetadataMetadataIntentsInfoBuilder::init()
    ->modelUuid('00000344-0000-0000-0000-000000000000')
    ->inputTokens(138)
    ->outputTokens(138)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

