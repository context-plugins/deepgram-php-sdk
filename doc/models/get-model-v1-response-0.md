
# Get Model V1 Response 0

*This model accepts additional fields of type array.*

## Structure

`GetModelV1Response0`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `name` | `?string` | Optional | - | getName(): ?string | setName(?string name): void |
| `canonicalName` | `?string` | Optional | - | getCanonicalName(): ?string | setCanonicalName(?string canonicalName): void |
| `architecture` | `?string` | Optional | - | getArchitecture(): ?string | setArchitecture(?string architecture): void |
| `languages` | `?(string[])` | Optional | - | getLanguages(): ?array | setLanguages(?array languages): void |
| `version` | `?string` | Optional | - | getVersion(): ?string | setVersion(?string version): void |
| `uuid` | `?string` | Optional | - | getUuid(): ?string | setUuid(?string uuid): void |
| `batch` | `?bool` | Optional | - | getBatch(): ?bool | setBatch(?bool batch): void |
| `streaming` | `?bool` | Optional | - | getStreaming(): ?bool | setStreaming(?bool streaming): void |
| `formattedOutput` | `?bool` | Optional | - | getFormattedOutput(): ?bool | setFormattedOutput(?bool formattedOutput): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\GetModelV1Response0Builder;
use DeepgramLib\ApiHelper;

$getModelV1Response0 = GetModelV1Response0Builder::init()
    ->name('name6')
    ->canonicalName('canonical_name8')
    ->architecture('architecture4')
    ->languages(
        [
            'languages3',
            'languages4'
        ]
    )
    ->version('version2')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

