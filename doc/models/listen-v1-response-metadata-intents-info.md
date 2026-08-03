
# Listen V1 Response Metadata Intents Info

*This model accepts additional fields of type array.*

## Structure

`ListenV1ResponseMetadataIntentsInfo`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `modelUuid` | `?string` | Optional | - | getModelUuid(): ?string | setModelUuid(?string modelUuid): void |
| `inputTokens` | `?int` | Optional | - | getInputTokens(): ?int | setInputTokens(?int inputTokens): void |
| `outputTokens` | `?int` | Optional | - | getOutputTokens(): ?int | setOutputTokens(?int outputTokens): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\ListenV1ResponseMetadataIntentsInfoBuilder;
use RestApiLib\ApiHelper;

$listenV1ResponseMetadataIntentsInfo = ListenV1ResponseMetadataIntentsInfoBuilder::init()
    ->modelUuid('model_uuid8')
    ->inputTokens(178)
    ->outputTokens(178)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

