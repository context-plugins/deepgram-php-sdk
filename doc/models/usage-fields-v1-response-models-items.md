
# Usage Fields V1 Response Models Items

*This model accepts additional fields of type array.*

## Structure

`UsageFieldsV1ResponseModelsItems`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `name` | `?string` | Optional | Name of the model. | getName(): ?string | setName(?string name): void |
| `language` | `?string` | Optional | The language supported by the model (IETF language tag). | getLanguage(): ?string | setLanguage(?string language): void |
| `version` | `?string` | Optional | Version identifier of the model, typically with a date and a revision number. | getVersion(): ?string | setVersion(?string version): void |
| `modelId` | `?string` | Optional | Unique identifier for the model. | getModelId(): ?string | setModelId(?string modelId): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\UsageFieldsV1ResponseModelsItemsBuilder;
use DeepgramLib\ApiHelper;

$usageFieldsV1ResponseModelsItems = UsageFieldsV1ResponseModelsItemsBuilder::init()
    ->name('name4')
    ->language('language6')
    ->version('version0')
    ->modelId('model_id4')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

