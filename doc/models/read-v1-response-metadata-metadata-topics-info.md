
# Read V1 Response Metadata Metadata Topics Info

*This model accepts additional fields of type array.*

## Structure

`ReadV1ResponseMetadataMetadataTopicsInfo`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `modelUuid` | `?string` | Optional | - | getModelUuid(): ?string | setModelUuid(?string modelUuid): void |
| `inputTokens` | `?int` | Optional | - | getInputTokens(): ?int | setInputTokens(?int inputTokens): void |
| `outputTokens` | `?int` | Optional | - | getOutputTokens(): ?int | setOutputTokens(?int outputTokens): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\ReadV1ResponseMetadataMetadataTopicsInfoBuilder;
use RestApiLib\ApiHelper;

$readV1ResponseMetadataMetadataTopicsInfo = ReadV1ResponseMetadataMetadataTopicsInfoBuilder::init()
    ->modelUuid('000011b4-0000-0000-0000-000000000000')
    ->inputTokens(250)
    ->outputTokens(250)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

