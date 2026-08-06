
# List Models V1 Response Tts Models

*This model accepts additional fields of type array.*

## Structure

`ListModelsV1ResponseTtsModels`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `name` | `?string` | Optional | - | getName(): ?string | setName(?string name): void |
| `canonicalName` | `?string` | Optional | - | getCanonicalName(): ?string | setCanonicalName(?string canonicalName): void |
| `architecture` | `?string` | Optional | - | getArchitecture(): ?string | setArchitecture(?string architecture): void |
| `languages` | `?(string[])` | Optional | - | getLanguages(): ?array | setLanguages(?array languages): void |
| `version` | `?string` | Optional | - | getVersion(): ?string | setVersion(?string version): void |
| `uuid` | `?string` | Optional | - | getUuid(): ?string | setUuid(?string uuid): void |
| `metadata` | [`?ListModelsV1ResponseTtsModelsMetadata`](../../doc/models/list-models-v1-response-tts-models-metadata.md) | Optional | - | getMetadata(): ?ListModelsV1ResponseTtsModelsMetadata | setMetadata(?ListModelsV1ResponseTtsModelsMetadata metadata): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\ListModelsV1ResponseTtsModelsBuilder;
use DeepgramLib\ApiHelper;

$listModelsV1ResponseTtsModels = ListModelsV1ResponseTtsModelsBuilder::init()
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
    ->build();
```

