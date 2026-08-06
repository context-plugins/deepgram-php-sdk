
# Usage Fields V1 Response

*This model accepts additional fields of type array.*

## Structure

`UsageFieldsV1Response`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `tags` | `?(string[])` | Optional | List of tags associated with the project | getTags(): ?array | setTags(?array tags): void |
| `models` | [`?(UsageFieldsV1ResponseModelsItems[])`](../../doc/models/usage-fields-v1-response-models-items.md) | Optional | List of models available for the project. | getModels(): ?array | setModels(?array models): void |
| `processingMethods` | `?(string[])` | Optional | Processing methods supported by the API | getProcessingMethods(): ?array | setProcessingMethods(?array processingMethods): void |
| `features` | `?(string[])` | Optional | API features available to the project | getFeatures(): ?array | setFeatures(?array features): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\UsageFieldsV1ResponseBuilder;
use DeepgramLib\Models\Builders\UsageFieldsV1ResponseModelsItemsBuilder;
use DeepgramLib\ApiHelper;

$usageFieldsV1Response = UsageFieldsV1ResponseBuilder::init()
    ->tags(
        [
            'tags3'
        ]
    )
    ->models(
        [
            UsageFieldsV1ResponseModelsItemsBuilder::init()
                ->name('name4')
                ->language('language6')
                ->version('version0')
                ->modelId('model_id4')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->processingMethods(
        [
            'processing_methods8',
            'processing_methods9'
        ]
    )
    ->features(
        [
            'features9',
            'features0',
            'features1'
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

