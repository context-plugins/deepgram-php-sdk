
# List Models V1 Response

*This model accepts additional fields of type array.*

## Structure

`ListModelsV1Response`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `stt` | [`?(ListModelsV1ResponseSttModels[])`](../../doc/models/list-models-v1-response-stt-models.md) | Optional | - | getStt(): ?array | setStt(?array stt): void |
| `tts` | [`?(ListModelsV1ResponseTtsModels[])`](../../doc/models/list-models-v1-response-tts-models.md) | Optional | - | getTts(): ?array | setTts(?array tts): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\ListModelsV1ResponseBuilder;
use RestApiLib\Models\Builders\ListModelsV1ResponseSttModelsBuilder;
use RestApiLib\ApiHelper;
use RestApiLib\Models\Builders\ListModelsV1ResponseTtsModelsBuilder;

$listModelsV1Response = ListModelsV1ResponseBuilder::init()
    ->stt(
        [
            ListModelsV1ResponseSttModelsBuilder::init()
                ->name('name6')
                ->canonicalName('canonical_name8')
                ->architecture('architecture4')
                ->languages(
                    [
                        'languages3',
                        'languages4',
                        'languages5'
                    ]
                )
                ->version('version2')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            ListModelsV1ResponseSttModelsBuilder::init()
                ->name('name6')
                ->canonicalName('canonical_name8')
                ->architecture('architecture4')
                ->languages(
                    [
                        'languages3',
                        'languages4',
                        'languages5'
                    ]
                )
                ->version('version2')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->tts(
        [
            ListModelsV1ResponseTtsModelsBuilder::init()
                ->name('name2')
                ->canonicalName('canonical_name2')
                ->architecture('architecture0')
                ->languages(
                    [
                        'languages1'
                    ]
                )
                ->version('version8')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            ListModelsV1ResponseTtsModelsBuilder::init()
                ->name('name2')
                ->canonicalName('canonical_name2')
                ->architecture('architecture0')
                ->languages(
                    [
                        'languages1'
                    ]
                )
                ->version('version8')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

