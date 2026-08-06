
# Get Model V1 Response 1

*This model accepts additional fields of type array.*

## Structure

`GetModelV1Response1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `name` | `?string` | Optional | - | getName(): ?string | setName(?string name): void |
| `canonicalName` | `?string` | Optional | - | getCanonicalName(): ?string | setCanonicalName(?string canonicalName): void |
| `architecture` | `?string` | Optional | - | getArchitecture(): ?string | setArchitecture(?string architecture): void |
| `languages` | `?(string[])` | Optional | - | getLanguages(): ?array | setLanguages(?array languages): void |
| `version` | `?string` | Optional | - | getVersion(): ?string | setVersion(?string version): void |
| `uuid` | `?string` | Optional | - | getUuid(): ?string | setUuid(?string uuid): void |
| `metadata` | [`?GetModelV1ResponseOneOf1Metadata`](../../doc/models/get-model-v1-response-one-of-1-metadata.md) | Optional | - | getMetadata(): ?GetModelV1ResponseOneOf1Metadata | setMetadata(?GetModelV1ResponseOneOf1Metadata metadata): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\GetModelV1Response1Builder;
use DeepgramLib\ApiHelper;

$getModelV1Response1 = GetModelV1Response1Builder::init()
    ->name('name6')
    ->canonicalName('canonical_name8')
    ->architecture('architecture4')
    ->languages(
        [
            'languages3'
        ]
    )
    ->version('version2')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

