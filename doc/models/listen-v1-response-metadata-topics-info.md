
# Listen V1 Response Metadata Topics Info

*This model accepts additional fields of type array.*

## Structure

`ListenV1ResponseMetadataTopicsInfo`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `modelUuid` | `?string` | Optional | - | getModelUuid(): ?string | setModelUuid(?string modelUuid): void |
| `inputTokens` | `?int` | Optional | - | getInputTokens(): ?int | setInputTokens(?int inputTokens): void |
| `outputTokens` | `?int` | Optional | - | getOutputTokens(): ?int | setOutputTokens(?int outputTokens): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\ListenV1ResponseMetadataTopicsInfoBuilder;
use DeepgramLib\ApiHelper;

$listenV1ResponseMetadataTopicsInfo = ListenV1ResponseMetadataTopicsInfoBuilder::init()
    ->modelUuid('model_uuid6')
    ->inputTokens(24)
    ->outputTokens(24)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

