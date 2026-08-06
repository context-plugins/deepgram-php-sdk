
# Listen V1 Response Metadata Summary Info

*This model accepts additional fields of type array.*

## Structure

`ListenV1ResponseMetadataSummaryInfo`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `modelUuid` | `?string` | Optional | - | getModelUuid(): ?string | setModelUuid(?string modelUuid): void |
| `inputTokens` | `?int` | Optional | - | getInputTokens(): ?int | setInputTokens(?int inputTokens): void |
| `outputTokens` | `?int` | Optional | - | getOutputTokens(): ?int | setOutputTokens(?int outputTokens): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\ListenV1ResponseMetadataSummaryInfoBuilder;
use DeepgramLib\ApiHelper;

$listenV1ResponseMetadataSummaryInfo = ListenV1ResponseMetadataSummaryInfoBuilder::init()
    ->modelUuid('model_uuid8')
    ->inputTokens(104)
    ->outputTokens(104)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

